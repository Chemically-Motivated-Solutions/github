# Chemically motivated Solutions - Retro Terminal

A retro-style hacker terminal interface with customizable themes and responsive design. Experience the nostalgic feel of classic computer terminals with modern features and functionality.

![Terminal Preview](preview.png)

## Features

- 🎨 **Customizable Themes**: Switch between light and dark modes
- ⌨️ **Command Autocompletion**: Tab completion for commands and arguments
- 📜 **Command History**: Navigate through previous commands using arrow keys
- 🎬 **Boot Sequence Animation**: Authentic retro-style startup sequence
- 📺 **CRT Effects**: Scanlines and power-on animations
- 📱 **Responsive Design**: Works on all screen sizes
- 🔧 **Multiple Built-in Commands**: Various utility commands with argument support

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/retro-terminal.git
cd retro-terminal
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
python main.py
```

The terminal will be available at `http://localhost:5000`

## Usage

### Available Commands

Use `help` to see all available commands. Here are some examples:

- `help [--all] [--short]` - Show available commands and their arguments
- `clear` - Clear the terminal screen
- `echo [text] [--color] [--newline] [--repeat]` - Display text
- `date [--format=short|long] [--utc]` - Show current date
- `time [--format=12h|24h] [--zone=UTC]` - Show current time
- `ls [-l] [-a] [--sort=name|date]` - List directory contents
- `version [--full] [--build]` - Show terminal version
- `about` - Display information about the terminal

### Command Autocompletion

1. Press `Tab` to autocomplete commands
2. For commands with arguments, type `--` and press `Tab` to see available options
3. Press `Tab` multiple times to cycle through suggestions

### Theme Customization

Click the theme toggle button (☀️/🌙) in the terminal header to switch between light and dark themes.

## Development

### Project Structure

```
retro-terminal/
├── static/
│   ├── css/
│   │   └── terminal.css    # Styling and themes
│   └── js/
│       ├── terminal.js     # Core terminal functionality
│       └── themes.js       # Theme management
├── templates/
│   └── index.html         # Main terminal interface
├── app.py                 # Flask application
└── main.py               # Entry point
```

### Adding New Commands

To add a new command, extend the `commands` object in `terminal.js`:

```javascript
commands: {
    'new-command': {
        fn: (args) => this.newCommandFunction(args),
        desc: 'Description of the command',
        args: ['--argument1', '--argument2']  // Optional arguments
    }
}
```

### Custom Themes

Themes are defined in `terminal.css`. Add new themes by following this pattern:

```css
[data-theme="custom-theme"] {
    --bg-primary: #your-color;
    --bg-secondary: #your-color;
    --text-primary: #your-color;
    --text-secondary: #your-color;
    --glow-color: rgba(r, g, b, a);
}
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
