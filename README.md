# Electron App Starter

A robust, modern starter template for building cross-platform desktop applications with Electron, TypeScript, and Vite.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Electron](https://img.shields.io/badge/electron-35.0.2-blue.svg)
![TypeScript](https://img.shields.io/badge/typescript-4.5.4-blue.svg)
![Vite](https://img.shields.io/badge/vite-5.4.14-blue.svg)

## 🚀 Features

- **Modern Stack**: Electron 35, TypeScript 4.5, and Vite 5.4
- **Type Safety**: Full TypeScript integration throughout the codebase
- **Fast Development**: Hot reloading with Vite for rapid development
- **Secure Architecture**: Proper process isolation with security best practices
- **Cross-Platform**: Build for Windows, macOS, and Linux with a single codebase
- **Easy Packaging**: Simple commands to create distributable installers
- **Quality Assurance**: ESLint configuration for code quality enforcement
- **Optimized Production**: Efficient bundling and packaging for production builds

## 📋 Prerequisites

- Node.js 18+ and npm
- Git

## 🔧 Quick Start

```bash
# Clone the repository
git clone https://github.com/rmncldyo/electron-app-starter.git
cd electron-app-starter

# Install dependencies
npm install

# Start the development server
npm start
```

## 📦 Project Structure

```
electron-app-starter/
├── src/                   # Source code
│   ├── main.ts            # Main process entry point
│   ├── preload.ts         # Preload script for secure IPC
│   ├── renderer.ts        # Renderer process logic
│   └── index.css          # Basic styling
├── index.html             # Main HTML template
├── forge.config.ts        # Electron Forge configuration
├── vite.main.config.ts    # Vite config for main process
├── vite.preload.config.ts # Vite config for preload scripts
├── vite.renderer.config.ts # Vite config for renderer process
├── tsconfig.json          # TypeScript configuration
└── package.json           # Project dependencies and scripts
```

## 🏗️ Architecture

This application follows Electron's recommended architecture with three main components:

1. **Main Process** (`src/main.ts`)
   - Application entry point
   - Window management
   - Native OS interactions
   - IPC handling

2. **Renderer Process** (`src/renderer.ts`, `index.html`)
   - User interface
   - Web technologies (HTML, CSS, JS)
   - Secure interaction with main process via IPC

3. **Preload Scripts** (`src/preload.ts`)
   - Security bridge between main and renderer
   - Exposes only allowed APIs to renderer
   - Handles IPC communication

## 📜 Available Scripts

- `npm start` - Start the application in development mode
- `npm run package` - Package the app without creating installers
- `npm run make` - Create platform-specific distributables (installers, etc.)
- `npm run publish` - Publish the application
- `npm run lint` - Lint the codebase using ESLint

## 🔒 Security Features

- Context isolation enabled by default
- Node integration disabled in renderer process
- Secure IPC communication pattern
- Content Security Policy implementation
- Electron Fuses for additional security hardening

## 📱 Cross-Platform Support

The application can be packaged for:
- Windows (NSIS installer, Squirrel.Windows)
- macOS (.app, .dmg)
- Linux (.deb, .rpm)

## 🔄 Development Workflow

1. Make changes to the source code
2. See changes instantly with hot reloading
3. Use `npm run lint` to check for code issues
4. Package your application with `npm run make`

## 📦 Building for Production

```bash
# Create packages for current platform
npm run make

# For specific platforms (if supported by your OS)
npm run make -- --platform=win32 (windowsOS)
npm run make -- --platform=darwin (macOS)
npm run make -- --platform=linux (linuxOS)
```

## 🛠️ Customization

### Application Information
Edit `package.json` to update:
- Application name
- Description
- Version
- Author information

### Build Configuration
Modify `forge.config.ts` to change:
- Packaging options
- Installer configurations
- Platform-specific settings

### UI Framework Integration
The starter is ready to integrate with popular UI frameworks:
- React
- Vue
- Svelte

## 🧩 Planned Features

- Secure IPC communication implementation
- Error handling and logging system
- UI framework integration (React/Vue/Svelte)
- State management solution
- Testing infrastructure
- Auto-updates capability

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📚 Resources

- [Electron Documentation](https://www.electronjs.org/docs)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
- [Vite Documentation](https://vitejs.dev/guide/)
- [Electron Forge Documentation](https://www.electronforge.io/)