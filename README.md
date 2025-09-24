<img width="700" height="548" alt="splash" src="https://github.com/user-attachments/assets/70a5cd5a-ce34-43af-b592-4983b5b4fa57" />


# Creator Assistant
### A Modern YouTube Comment Bot: By PrimeTools

## Table of Contents
1. [Overview](#overview)
2. [Installation & Setup](#installation--setup)
3. [Getting Started](#getting-started)
4. [Main Features](#main-features)
5. [Account Management](#account-management)
6. [Settings Configuration](#settings-configuration)
7. [Comment Templates & Spintax](#comment-templates--spintax)
8. [Running the Bot](#running-the-bot)
9. [Monitoring & Status](#monitoring--status)
10. [Troubleshooting](#troubleshooting)
11. [Best Practices](#best-practices)
12. [FAQ](#faq)

---
![](https://imgur.com/9CuLdTf.png)
![](https://imgur.com/NjyLLeo.png)
![](https://imgur.com/fw0u0vB.png)
![](https://imgur.com/3f5VSPD.png)
![](https://imgur.com/lq0cyVL.png)

## Overview

The YouTube Comment Bot is a powerful automation tool designed to help content creators and marketers engage with YouTube videos through intelligent commenting. The bot supports multiple YouTube accounts, advanced filtering options, and sophisticated comment generation using spintax templates.

### Key Features
- **Multi-Account Support**: Manage and rotate between multiple YouTube accounts
- **Smart Commenting**: Skip videos you've already commented on
- **Advanced Filtering**: Filter videos by upload date, view count, comment count, and duration
- **Spintax Support**: Create varied comments using nested spintax syntax
- **Scheduling**: Set specific times for comment posting
- **Dry Run Mode**: Test your setup without actually posting comments
- **Real-time Monitoring**: Track success/failure rates and comment history

---

## Installation & Setup

### System Requirements
- Windows 10/11
- Internet connection
- YouTube account(s) with commenting permissions

### Installation Steps

1. **Download the Application**
   - Download the latest version from your distribution source
   - The application comes as a single executable file

2. **First Launch**
   - Run the executable file
   - No additional setup required

3. **Client Secret Setup**
   - The application includes pre-configured client secrets
   - No manual configuration needed for basic usage

---

## Getting Started

### Initial Setup

1. **Launch the Application**
   - Double-click the executable to start
   - Wait for the splash screen to complete
   
2. **Authenticate Your YouTube Account**
   - Go to the "Accounts" tab
   - Click "Add Account"
   - Follow the authentication process in your browser
   - Make sure that your YouTube accounts have a "channel" created

3. **Configure Basic Settings**
   - Set your keywords in the "Main" tab
   - Add your comment templates
   - Configure basic bot settings

## Main Features

### Main Tab - Core Functionality

#### Keywords Section
- **Purpose**: Define what videos the bot should search for
- **Format**: Comma-separated keywords (e.g., "python tutorial, coding tips, programming")
- **Tips**: Use specific, relevant keywords for better targeting

#### Comments Section
- **Purpose**: Define what comments to post
- **Spintax Support**: Use `{option1|option2|option3}` for variation
- **Nested Spintax**: `{Great|Awesome|Amazing} {video|content|tutorial}! {Thanks|Appreciate} for sharing.`
- **Multiple Comments**: Add one comment template per line

#### Spintax Helper
- **Real-time Preview**: See how many unique variations your templates will generate
- **Length Analysis**: Monitor minimum and maximum comment lengths
- **Validation**: Ensure your spintax syntax is correct

### Settings Tab - Advanced Configuration

#### Video Filters

**Videos per Keyword**
- Set how many videos to process for each keyword
- Recommended: 3-5 for balanced activity

**Delay Settings**
- **Format**: `min,max` (e.g., "90,180" for 90-180 seconds between comments)
- **Purpose**: Avoid detection and respect YouTube's rate limits
- **Recommended**: 120-300 seconds for safety

**Upload Date Filter**
- **Anytime**: No date restrictions
- **Last Hour**: Very recent videos only
- **Today**: Videos uploaded today
- **This Week**: Videos from the past week
- **This Month**: Videos from the past month
- **This Year**: Videos from the current year

**View Count Filter**
- **Min Views**: Minimum view count (e.g., 1000)
- **Max Views**: Maximum view count (e.g., 100000)
- **Purpose**: Target videos with an appropriate audience size

**Comments Count Filter**
- **Min Comments**: Minimum comment count
- **Max Comments**: Maximum comment count
- **Purpose**: Target videos with active engagement

**Video Duration Filter**
- **Any**: No duration restrictions
- **Short (<4 min)**: Quick videos
- **Medium (4-20 min)**: Standard length
- **Long (>20 min)**: Long-form content

#### Advanced Options

**Dry Run Mode**
- **Purpose**: Test your configuration without posting actual comments
- **Use Case**: Perfect for testing new templates and settings
- **Output**: All actions are logged, but no comments are posted

## Account Management

### Adding Accounts

1. **Navigate to Accounts Tab**
2. **Click "Add Account"**
3. **Complete Authentication**
   - Browser will open for YouTube authentication
   - Grant necessary permissions
   - Account will be added to your "authenticated" directory

### Account Features

**Account Rotation**
- **Automatic**: Bot can cycle through accounts for each comment
- **Manual Selection**: Choose a specific account for next job
- **Status Tracking**: Monitor which accounts are active

**Account Information**
- **Channel Name**: Display name of the YouTube channel
- **Last Used**: Timestamp of last activity
- **Status**: Active/Inactive status

### Managing Multiple Accounts

**Best Practices**
- Use 3-5 accounts for optimal performance
- Ensure accounts have different IP addresses (use proxies if needed)
- Rotate accounts regularly to avoid detection
- Monitor account health and quota limits

---

## Settings Configuration

### Basic Settings

**Videos per Keyword**
- **Range**: less than 50 recommended
- **Purpose**: Control how many videos to process per keyword
- **Balance**: More videos = more activity, but higher risk

**Delay Between Comments**
- **Minimum**: 60 seconds (absolute minimum)
- **Recommended**: 120-300 seconds
- **Maximum**: 600+ seconds for maximum safety
- If cycling multi accounts, the more accs you use = the lower delay you can put

### Advanced Filtering

**Upload Date Strategy**
- **Recent Content**: Use "Last Hour" or "Today" for trending topics
- **Established Content**: Use "This Week" or "This Month" for stable engagement
- **Evergreen Content**: Use "Anytime" for broad reach

**View Count Strategy**
- **New Channels**: Target 100-10,000 views
- **Growing Channels**: Target 1,000-100,000 views
- **Established Channels**: Target 10,000+ views

**Comment Count Strategy**
- **Active Communities**: Target videos with 10+ comments
- **Growing Engagement**: Target videos with 5-50 comments
- **New Content**: Target videos with 0-10 comments

---

## Comment Templates & Spintax

### Basic Spintax Syntax

**Simple Variations**
```
{Great|Awesome|Amazing} video!
```

**Multiple Variations**
```
{Thanks|Appreciate} for the {helpful|useful|valuable} {tutorial|guide|tips}!
```

### Advanced Spintax

**Nested Variations**
```
This is {so {helpful|useful}|{absolutely|really} {amazing|incredible}}! I {can't believe|never thought} I'd {find|come across} something like this.
```

**Context-Aware Comments**
```
AI-powered context-aware comments are Coming Soon!
```

### Spintax Best Practices

**Variation Guidelines**
- Use 3-5 options per variation for optimal diversity
- Keep variations similar in length and tone
- Test templates with the Spintax Helper before using

**Content Guidelines**
- Keep comments genuine and relevant
- Avoid spammy language
- Use proper grammar and spelling
- Match the video's tone and content

## Running the Bot

### Starting the Bot

1. **Verify Settings**
   - Check keywords and comment templates
   - Confirm account authentication
   - Review filter settings

2. **Choose Mode**
   - **Live Mode**: Default
   - **Dry Run**: Test without posting (recommended first)

3. **Start the Bot**
   - Click "Start Bot" in the Main tab
   - Monitor progress in the Status tab

### Bot Operation

**Search Process**
1. Bot searches for videos using your keywords
2. Applies filters (date, views, comments, duration)
3. Checks if you've already commented
4. Generates comment using spintax
5. Posts comment (if not in dry run mode)
6. Waits for specified delay
7. Repeats for next video

**Account Rotation Mode**
- Bot automatically cycles through authenticated accounts
- Each comment uses a different account
- Prevents overuse of individual accounts

### Monitoring Progress

**Status Tab Features**
- **Real-time Logs**: See what the bot is doing
- **Success/Failure Counters**: Track performance
- **Error Logs**: Identify and resolve issues
- **Comment History**: Review posted comments

## Monitoring & Status

### Status Tab Overview

**Live Activity Feed**
- Real-time updates of bot activity
- Search results and video information
- Comment posting confirmations
- Error messages and warnings

**Performance Metrics**
- **Success Rate**: Percentage of successful comments
- **Total Comments**: Number of comments posted
- **Failed Attempts**: Comments that couldn't be posted
- **Account Status**: Health of authenticated accounts

### Error Monitoring

**Common Issues**
- **Authentication Errors**: Account needs re-authentication
- **Quota Exceeded**: Daily comment limit reached
- **Network Issues**: Connection problems
- **Video Restrictions**: Comments disabled on video

**Error Resolution**
- Check account authentication status
- Verify network connection
- Review video-specific restrictions
- Adjust delay settings if needed

---

## 🔧 Recent Updates (v0.1.9)

### ✅ Fixed Issues
- **Quota Detection**: Fixed overly aggressive quota exceeded detection
- **Comment Verification**: Improved comment verification reliability
- **Error Handling**: Better error messages and recovery
- **Syntax Fixes**: Resolved compilation issues

### 🆕 New Features
- **Enhanced Verification**: More reliable comment posting confirmation
- **Better Quota Management**: Smarter client secret cycling
- **Improved Error Messages**: Clearer feedback on issues
- **Robust Verification**: Multiple verification methods for comments

### 🔧 Technical Improvements
- **Processing Delays**: Added delays for YouTube comment processing
- **Author ID Verification**: Check comments by channel ID
- **Dual Search Methods**: Multiple verification approaches
- **Better Text Matching**: Exact and partial match detection

---

## Troubleshooting

### Common Issues

**Bot Won't Start**
- **Check Authentication**: Ensure at least one account is authenticated
- **Verify Keywords**: Make sure keywords are entered
- **Review Settings**: Check all required settings are configured

**No Videos Found**
- **Broaden Keywords**: Use more general terms
- **Adjust Filters**: Relax view count or date restrictions
- **Check Keywords**: Ensure keywords are relevant and popular

**Comments Not Posting**
- **Check Account Status**: Verify accounts are authenticated
- **Review Quota Limits**: Accounts may have reached daily limits
- **Verify Video Settings**: Some videos may have comments disabled

**High Failure Rate**
- **Increase Delays**: Longer delays between comments
- **Check Account Health**: Some accounts may be flagged
- **Review Comment Templates**: Ensure comments are appropriate

### Performance Optimization

**Speed vs. Safety**
- **Fast Mode**: 60-120 second delays (higher risk)
- **Balanced Mode**: 120-300 second delays (recommended)
- **Safe Mode**: 300+ second delays (maximum safety)

**Account Management**
- **Regular Rotation**: Use 3-5 accounts
- **Monitor Health**: Watch for quota issues
- **IP Diversity**: Use different IP addresses if possible

---

## Best Practices

### Comment Strategy

**Quality Over Quantity**
- Focus on relevant, valuable comments
- Avoid generic or spammy language
- Engage genuinely with content

**Template Design**
- Create multiple variations
- Test templates before using
- Keep comments concise but meaningful

### Account Management

**Account Health**
- Don't overuse individual accounts
- Monitor quota limits regularly
- Rotate accounts frequently

**Safety Measures**
- Use appropriate delays
- Avoid commenting on restricted content
- Monitor for account warnings

### Content Strategy

**Keyword Selection**
- Use specific, relevant keywords
- Avoid overly broad terms
- Research trending topics

**Targeting Strategy**
- Focus on videos with moderate engagement
- Avoid over-saturated content
- Target channels in your niche

## FAQ

### General Questions

**Q: Is this tool safe to use?**
A: Yes, when used responsibly. Follow the guidelines, use appropriate delays, and avoid spammy behavior.

**Q: How many accounts should I use?**
A: 3-5 accounts is optimal. More accounts provide better rotation but require more management.

**Q: Can I get banned for using this tool?**
A: Following best practices minimizes risk. Use appropriate delays, quality comments, and don't overuse accounts.

### Technical Questions

**Q: Why is the bot not finding videos?**
A: Check your keywords, adjust filters, or try broader search terms.

**Q: How do I know if my comments are posting?**
A: Check the Status tab for real-time logs and success counters.

**Q: What if an account gets quota exceeded?**
A: The bot will automatically switch to other accounts. Wait 24 hours for quota reset.

### Settings Questions

**Q: What delay should I use?**
A: 120-300 seconds is recommended for safety. Longer delays are safer but slower.

**Q: How many videos per keyword?**
A: 3-5 videos per keyword is a good balance between activity and safety.

**Q: Should I use dry run mode?**
A: Yes, always test your setup with dry run mode before going live.

---

## Support & Updates

### Getting Help
- Check the Status tab for error messages
- Review the troubleshooting section
- Ensure all settings are configured correctly

### Updates
- The application includes automatic font installation
- No manual updates required for basic functionality
- Check for new versions periodically

### Safety Reminders
- Always use dry run mode for testing
- Monitor your accounts for any warnings
- Follow YouTube's community guidelines
- Use appropriate delays between comments

---

*This guide covers all major features and best practices for using the YouTube Comment Bot effectively and safely. For additional support or questions, refer to the troubleshooting section or contact your system administrator.*
