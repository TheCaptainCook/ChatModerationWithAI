# Minecraft AI Chat Moderator

A powerful Minecraft plugin that uses OpenAI's moderation API to automatically moderate chat messages in real-time. The plugin checks messages against various categories of inappropriate content and can block messages that exceed configured thresholds.

## Features

- Real-time chat moderation using OpenAI's moderation API
- Configurable moderation thresholds for different categories
- Link detection and whitelist system
- High-performance caching system:
    - In-memory LRU cache
    - Configurable cache size and duration
    - Thread-safe implementation
    - Automatic cleanup of expired entries
- Async processing for optimal performance
- Admin notifications for blocked messages
- Configurable warning messages
- Permission-based bypass system
- Detailed logging options
- Easy configuration
- Comprehensive test coverage

## Requirements

- Spigot/Paper 1.21.4
- Java 17 or higher
- OpenAI API key

## Installation

1. Download the latest release from the releases page
2. Place the JAR file in your server's `plugins` folder
3. Restart your server
4. Configure your OpenAI API key in `plugins/MinecraftAIChatModerator/config.yml`

## Configuration

The plugin is highly configurable through the `config.yml` file. Here are the main configuration sections:

### OpenAI API Settings
```yaml
openai:
  api-key: "your-api-key-here"
  endpoint: "https://api.openai.com/v1/moderations"
  request-timeout: 5000
```

### Moderation Categories
Each category can be enabled/disabled and has configurable thresholds and warning messages:
```yaml
moderation:
  categories:
    harassment:
      enabled: true
      threshold: 0.8
      warning: "&cYour message was blocked for harassment."
```

### Link Detection
```yaml
links:
  enabled: true
  warning: "&cLinks are not allowed in chat!"
  whitelist:
    - "minecraft.net"
    - "spigotmc.org"
```

## Permissions

- `aichatmod.admin` - Access to admin commands and notifications
- `aichatmod.bypass` - Bypass chat moderation

## Commands

- `/aichatmod reload` - Reload the configuration
- `/aichatmod stats` - View moderation statistics

## Moderation Categories

The plugin checks messages against the following categories:

- Harassment
- Hate Speech
- Sexual Content
- Violence
- Self-harm
- Illicit Activities
- And more...

Each category has configurable thresholds and custom warning messages.

## Development

Built with:
- Maven
- Spigot API 1.21.4
- Java 17
- Gson for JSON processing

### Testing

Run the test suite:
```bash
mvn test
```

The project includes:
- Unit tests for core functionality
- Integration tests for API communication
- Performance tests for caching system
- Mock-based tests for Bukkit/Spigot components

### Building from Source

1. Clone the repository
2. Run `mvn clean package`
3. Find the built jar in `target/`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under GNU General Public License v3.0 - see the [LICENSE](https://github.com/TheCaptainCook/ChatModerationWithAI/blob/main/LICENSE) file for details.

## Support

If you encounter any issues or need help, please:
1. Check the [Wiki](https://github.com/TheCaptainCook/ChatModerationWithAI/wiki) for documentation
2. Open an [Issue](https://github.com/TheCaptainCook/ChatModerationWithAI/issues) on GitHub
3. Send me a mail - [The Captain Cook](mailto:Masem@duck.com)

## Credits

- OpenAI for providing the moderation API
- Spigot/Paper team for the Minecraft server software
- The Minecraft plugin development community

## Changelog

### Version 1.0.0
- Initial release
- Basic moderation functionality
- Link detection
- Admin notifications
- Configuration system
