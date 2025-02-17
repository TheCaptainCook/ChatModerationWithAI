# Minecraft Chat Moderator Plugin

A powerful Minecraft plugin that uses OpenAI's moderation API to automatically moderate chat messages in real-time.

## Features

- Real-time chat moderation using OpenAI's moderation API
- Configurable moderation thresholds
- Customizable warning messages
- Link detection and blocking
- Efficient caching system to reduce API calls
- Detailed logging system
- Permission-based administration

## Requirements

- Spigot 1.21.4
- Java 17 or higher
- OpenAI API key

## Installation

1. Download the latest release from the releases page
2. Place the JAR file in your server's `plugins` folder
3. Restart your server
4. Configure your OpenAI API key in `config.yml`

## Configuration

The plugin is highly configurable through the `config.yml` file:

```yaml
# API Configuration
api:
  key: "your-openai-api-key"
  timeout: 5000  # milliseconds

# Moderation Thresholds (0.0 to 1.0)
thresholds:
  harassment: 0.7
  hate: 0.8
  sexual: 0.9
  violence: 0.8
  self-harm: 0.7

# Message Configuration
messages:
  blocked: "&cYour message was blocked due to inappropriate content."
  warning: "&eWarning: Your message contains potentially inappropriate content."

# Cache Configuration
cache:
  enabled: true
  duration: 3600  # seconds
```

## Permissions

- `chatmod.bypass` - Bypass chat moderation
- `chatmod.reload` - Reload plugin configuration
- `chatmod.admin` - Access to admin commands

## Commands

- `/chatmod reload` - Reload plugin configuration
- `/chatmod stats` - View moderation statistics
- `/chatmod test <message>` - Test message against moderation

## Support

For support, please:
1. Check the [Wiki](https://github.com/TheCaptainCook/ChatModerationWithAI/wiki)
2. Open an [Issue](https://github.com/TheCaptainCook/ChatModerationWithAI/issues)
3. Join our Discord (Work in Progress)