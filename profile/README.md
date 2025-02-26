# ReflexEngine

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/ReflexEngine/Reflex?style=social)](https://github.com/ReflexEngine/Reflex)

A high-performance, lightweight Lua runtime built in C that combines the simplicity of Lua with the power of LibUV for asynchronous I/O. ReflexEngine delivers exceptional scripting capabilities for applications requiring both speed and flexibility.

## 🚀 Features

- **Blazing Fast Performance**: Optimized C core with LuaJIT support for near-native execution speeds
- **Minimal Footprint**: Less than 50MB base installation with minimal dependencies
- **Asynchronous Architecture**: Built on LibUV for non-blocking I/O operations and event-driven programming
- **Dual Engine Support**: Use standard Lua for compatibility or LuaJIT for performance-critical applications
- **Embeddable Design**: Easily integrate into existing C/C++ applications with a clean API
- **Extensible Framework**: Add custom functionality through C modules or pure Lua libraries
- **Cross-Platform Compatibility**: First-class support for Windows, macOS, and Linux

## 📋 Requirements

- C99-compatible compiler (GCC 4.8+, Clang 3.4+, or MSVC 2015+)
- Make (alternative build option)
- Git (for source code management)

## 🔧 Installation

### From Source

```sh
# Clone the repository with submodules
git clone --recursive https://github.com/ReflexEngine/Reflex.git
cd Reflex

make
```

## 🏁 Quick Start

### Running Scripts

```sh
# Execute a Lua script
reflex run path/to/script.lua

# Pass arguments to your script
reflex run script.lua -- arg1 arg2

# Enable debug mode
reflex --debug run script.lua
```

### Interactive Shell

```sh
# Start the REPL
reflex
```

## 💻 Code Example

```lua
-- example.lua

-- Create an HTTP server
local server = reflex.http.createServer(function(req, res)
  res:writeHead(200, {['Content-Type'] = 'text/plain'})
  res:write('Hello from ReflexEngine!')
  res:finish()
end)

-- Start server and handle requests asynchronously
server:listen(3000, function()
  print('Server running at http://localhost:3000/')
end)
```

## 📚 Documentation

Comprehensive documentation is available at [Reflex's Github Wiki](https://github.com/ReflexEngine/reflex/wiki)

### API Reference Highlights

- Core API: `reflex.*` - Core runtime functions
- Process API: `process.*` - Process functions
- Environment API: `env.*` - Environment functions

## 🤝 Contributing

We welcome contributions from the community! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to your branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please see our [Contributing Guide](CONTRIBUTING.md) for more details.

## 📝 License

Copyright 2025 Reflex Team (Owned by AbdullahCXD)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## 👥 Community

- [GitHub Discussions](https://github.com/ReflexEngine/Reflex/discussions)
- [Discord Server](https://discord.gg/reflexengine)
- [Twitter](https://twitter.com/sabdullahcxd)

---

*Built with ❤️ by the ReflexEngine team and contributors.*
