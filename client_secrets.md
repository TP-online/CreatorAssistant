# 🔑 YouTube API Client Secret Setup Guide
 
> **Complete step-by-step instructions for creating your own YouTube API credentials**

## 📋 Table of Contents

1. [Why Create Your Own Client Secrets?](#why-create-your-own-client-secrets)
2. [Prerequisites](#prerequisites)
3. [Step-by-Step Setup](#step-by-step-setup)
4. [Installation in Bot](#installation-in-bot)
5. [Advanced Configuration](#advanced-configuration)
6. [Troubleshooting](#troubleshooting)
7. [FAQ](#faq)

---

## 🎯 Why Create Your Own Client Secrets?

### **Benefits:**
- **Higher Quota Limits**: Your own API keys have higher daily quotas
- **Better Control**: Manage your own API usage and billing
- **No Sharing**: Avoid quota conflicts with other users
- **Custom Branding**: Use your own Google Cloud project
- **Unlimited Accounts**: No restrictions on number of YouTube accounts

### **Quota Comparison:**
| Setup | Daily Quota | Comments/Day | Cost |
|--------|-------------|--------------|------|
| **Pre-configured** | ~1,000 units | ~20 comments | Free |
| **Your Own** | 10,000 units | ~200 comments | Free |
| **Multiple Projects** | 50,000+ units | 1,000+ comments | Free* |

*YouTube Data API has generous free tier - most users won't exceed limits

---

## ✅ Prerequisites

- Google account with YouTube access
- Valid YouTube channel
- Basic understanding of Google Cloud Console
- 15-20 minutes to complete setup
- Credit/debit card (for billing verification - usually no charges)

---

## 🚀 Step-by-Step Setup

### **Step 1: Create a Google Cloud Project**

1. **Go to Google Cloud Console**
   - Visit: https://console.cloud.google.com/
   - Sign in with your Google account

2. **Create New Project**
   - Click the project dropdown at the top
   - Click "New Project"
   - Enter project name: `YouTube Comment Bot`
   - Click "Create"

3. **Select Your Project**
   - Make sure your new project is selected in the dropdown

### **Step 2: Enable YouTube Data API v3**

1. **Navigate to APIs & Services**
   - In the left sidebar, click "APIs & Services"
   - Click "Library"

2. **Search for YouTube API**
   - Search for "YouTube Data API v3"
   - Click on "YouTube Data API v3"

3. **Enable the API**
   - Click "Enable"
   - Wait for activation (usually instant)

### **Step 3: Create OAuth 2.0 Credentials**

1. **Go to Credentials**
   - In the left sidebar, click "APIs & Services"
   - Click "Credentials"

2. **Create OAuth Consent Screen**
   - Click "OAuth consent screen"
   - Select "External" (unless you have Google Workspace)
   - Click "Create"

3. **Fill OAuth Consent Screen**
   - **App name**: `YouTube Comment Bot`
   - **User support email**: Your email
   - **Developer contact**: Your email
   - Click "Save and Continue"

4. **Skip Scopes (for now)**
   - Click "Save and Continue"
   - Click "Save and Continue" again

5. **Add Test Users (Important!)**
   - Click "Add Users"
   - Add your own email address
   - Click "Save and Continue"

### **Step 4: Create OAuth 2.0 Client ID**

1. **Create Credentials**
   - Go back to "Credentials"
   - Click "Create Credentials"
   - Select "OAuth 2.0 Client ID"

2. **Configure Application**
   - **Application type**: "Desktop application"
   - **Name**: `YouTube Comment Bot Desktop`
   - Click "Create"

3. **Download Credentials**
   - Click the download button (⬇️) next to your new client ID
   - Save the file as `client_secret.json`
   - **Important**: Keep this file secure!

### **Step 5: Configure OAuth Scopes**

1. **Edit OAuth Consent Screen**
   - Go to "OAuth consent screen"
   - Click "Edit App"

2. **Add Scopes**
   - Click "Add or Remove Scopes"
   - Search for and add these scopes:
     - `https://www.googleapis.com/auth/youtube.force-ssl`
     - `https://www.googleapis.com/auth/youtube.readonly`
   - Click "Update"
   - Click "Save and Continue"

### **Step 6: Set Up Billing (Required for Higher Quotas)**

1. **Go to Billing**
   - In the left sidebar, click "Billing"
   - Click "Link a billing account"

2. **Add Payment Method**
   - Add a credit/debit card
   - **Note**: YouTube Data API has a generous free tier
   - Most users won't exceed free limits

---

## 📁 Installation in Bot

### **Option 1: Simple Setup (Recommended)**

1. **Place in Root Directory**
   ```
   YouTube-Commentor/
   ├── app-v0.1.9.exe
   ├── client_secret.json          ← Place your file here!
   └── .env
   ```

2. **Run the Bot**
   - The bot will automatically detect and use your client secret
   - No additional configuration needed!

### **Option 2: Advanced Setup (Multiple Client Secrets)**

1. **Create Clients Directory**
   ```
   YouTube-Commentor/
   ├── app-v0.1.9.exe
   ├── clients/
   │   ├── client_secret1.json
   │   ├── client_secret2.json
   │   └── client_secret3.json
   └── .env
   ```

2. **Benefits of Multiple Client Secrets**
   - Higher total quota (10,000 units × number of secrets)
   - Better quota distribution
   - Redundancy if one secret hits quota

---

## 🔧 Advanced Configuration

### **Multiple Client Secrets Setup**

For maximum quota, create multiple client secrets:

1. **Create Multiple Google Cloud Projects**
   - Each project gets its own 10,000 unit quota
   - Use different Google accounts for each project
   - Repeat the setup process for each project

2. **File Naming Convention**
   ```
   clients/
   ├── client_secret1.json    (Project 1)
   ├── client_secret2.json    (Project 2)
   ├── client_secret3.json    (Project 3)
   └── client_secret4.json    (Project 4)
   ```

3. **Quota Calculation**
   - 1 project = 10,000 units/day = ~200 comments
   - 5 projects = 50,000 units/day = ~1,000 comments
   - 10 projects = 100,000 units/day = ~2,000 comments

### **Quota Management**

| Operation | Units Used | Comments Possible |
|-----------|------------|-------------------|
| Post Comment | ~50 | 200 per 10,000 units |
| Search Videos | ~100 | 100 per 10,000 units |
| Get Video Info | ~1 | 10,000 per 10,000 units |
| Check Comments | ~1 | 10,000 per 10,000 units |

### **Best Practices**

1. **Monitor Usage**: Check quota usage in Google Cloud Console
2. **Backup Credentials**: Keep secure backups of your client_secret.json files
3. **Rotate Keys**: Consider rotating client secrets monthly
4. **Use Multiple Projects**: Create separate Google Cloud projects for different client secrets

---

## 🚨 Troubleshooting

### **Common Issues & Solutions**

#### **"Quota exceeded" errors**
- **Cause**: Daily quota limit reached
- **Solution**: 
  - Wait 24 hours for quota reset
  - Create additional client secrets
  - Check quota usage in Google Cloud Console

#### **"Access blocked" errors**
- **Cause**: OAuth consent screen not configured properly
- **Solution**:
  - Verify OAuth consent screen is configured
  - Add your email to test users
  - Check that required scopes are added

#### **"Invalid client" errors**
- **Cause**: Incorrect client_secret.json file
- **Solution**:
  - Verify client_secret.json is in correct location
  - Check file format (should be valid JSON)
  - Ensure file is named correctly

#### **"This app isn't verified" warnings**
- **Cause**: App is in testing mode
- **Solution**:
  - Click "Advanced" → "Go to [App Name] (unsafe)"
  - This is normal for personal use
  - For production, submit for verification

### **Verification Steps**

1. **Check API is enabled:**
   - Go to APIs & Services > Library
   - Verify "YouTube Data API v3" shows "Enabled"

2. **Check credentials:**
   - Go to APIs & Services > Credentials
   - Verify your OAuth 2.0 Client ID exists

3. **Check scopes:**
   - Go to OAuth consent screen
   - Verify required scopes are listed

4. **Test the setup:**
   - Run the bot
   - Go to "Accounts" tab
   - Click "Add Account"
   - Complete OAuth flow

---

## 📊 Quota Optimization Tips

### **Maximize Your Quota**

1. **Use efficient searches**: Limit video results to what you need
2. **Less search filters**: leave more filters deactivated (set to 0)
3. **Cache results**: Avoid duplicate API calls
4. **Monitor usage**: Track quota consumption regularly
5. **Use Spintax mode**: AI Context-Aware Commenting uses exponentially more API calls

### **Scaling Strategies**

1. **Multiple Projects**: Create 5-10 Google Cloud projects
2. **Multiple Accounts**: Use different Google accounts for each project
3. **Quota Monitoring**: Set up alerts for quota usage
4. **Backup Plans**: Have multiple client secrets ready

### **Cost Management**

- **Free Tier**: 10,000 units per day per project
- **Most users**: Never exceed free limits
- **Heavy users**: Create multiple projects for higher quotas
- **Enterprise**: Consider Google Cloud billing for unlimited quotas

---

## 🎯 Quick Setup Checklist

- [ ] Google Cloud project created
- [ ] YouTube Data API v3 enabled
- [ ] OAuth consent screen configured
- [ ] OAuth 2.0 Client ID created
- [ ] Required scopes added
- [ ] Test users added
- [ ] Billing account linked
- [ ] client_secret.json downloaded
- [ ] File placed in bot directory
- [ ] Bot tested with new credentials

---

## 💡 Pro Tips

1. **Start Small**: Begin with one client secret, add more as needed
2. **Monitor Costs**: YouTube API is mostly free, but monitor usage
3. **Keep Backups**: Always backup your client_secret.json files
4. **Use Different Accounts**: Each Google account gets separate quota
5. **Test First**: Always test with dry run mode before going live
6. **Document Everything**: Keep track of which client secrets belong to which projects

---

## 🆘 FAQ

### **Q: Do I need to pay for YouTube API?**
A: No! The YouTube Data API has a generous free tier. Most users never exceed the free limits.

### **Q: How many comments can I post per day?**
A: With one client secret: ~200 comments. With 5 client secrets: ~1,000 comments.

### **Q: Can I use the bot without creating my own client secrets?**
A: Yes! The bot comes with pre-configured client secrets for basic usage.

### **Q: What if I hit quota limits?**
A: Create additional client secrets or wait 24 hours for quota reset.

### **Q: Is this setup secure?**
A: Yes! Your client_secret.json files are stored locally and never shared.

### **Q: Can I use multiple YouTube accounts?**
A: Yes! You can authenticate as many YouTube accounts as you want.

### **Q: What happens if I lose my client_secret.json file?**
A: You can download it again from Google Cloud Console, or create a new one.

---

## 🎉 Success!

Once you've completed this setup, you'll have:

- ✅ Your own YouTube API credentials
- ✅ Higher quota limits
- ✅ Full control over your API usage
- ✅ Ability to scale with multiple client secrets
- ✅ Professional setup for serious commenting campaigns

**Remember**: The bot works perfectly with the pre-configured client secrets, so this setup is optional but recommended for power users!

---

## 📞 Need Help?

If you encounter issues:

1. **Check the logs** in the bot's Status tab
2. **Verify all steps** were completed correctly
3. **Test with a simple setup** first
4. **Check Google Cloud Console** for error messages
5. **Ensure your YouTube channel** is properly set up

**Happy commenting!** 🚀
