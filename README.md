# 🎮 CppCraft - C++ Minecraft Engine

A complete conversion of the JavaScript-based **MineKhan** Minecraft clone to modern C++ with OpenGL.

## 🎯 Project Overview

CppCraft is an ambitious project to convert the fully-featured [MineKhan](https://github.com/Willard21/MineKhan) JavaScript Minecraft implementation into a high-performance C++ engine. MineKhan features over **4,600 lines** of JavaScript with complete world generation, block physics, inventory system, and WebGL rendering.

## 🚀 Target Features

### Core Engine Features
- **🎨 Modern OpenGL Rendering** - OpenGL 4.5+ with compute shaders
- **🌍 Infinite World Generation** - Perlin noise terrain, biomes, caves
- **🧱 50+ Block Types** - Full Minecraft block set with textures
- **⚡ Physics Engine** - Collision detection, gravity, water flow
- **👤 Player Controller** - FPS camera, movement, interaction
- **📦 Inventory System** - Crafting, item management, hotbar
- **🎵 Audio System** - 3D positional audio, music, SFX

### Advanced Features  
- **🌅 Day/Night Cycle** - Dynamic lighting, sky rendering
- **🧊 Water & Lava** - Fluid simulation and rendering
- **🔥 Particle Systems** - Break effects, weather, ambient
- **💾 World Persistence** - Save/load worlds with compression
- **🔧 Mod Support** - Plugin architecture for extensibility

## 🏗️ Architecture Plan

### Engine Modules
```
CppCraft/
├── src/                    # Source code
│   ├── core/              # Core engine systems
│   ├── rendering/         # OpenGL rendering pipeline  
│   ├── world/             # World generation & management
│   ├── physics/           # Physics & collision
│   ├── audio/             # Sound system
│   ├── input/             # Input handling
│   └── ui/                # User interface
├── include/               # Header files
├── shaders/               # GLSL shaders
├── textures/              # Block & UI textures
├── assets/                # Models, sounds, configs
└── docs/                  # Documentation
```

## 🔧 Technology Stack

- **Language**: Modern C++17/20
- **Graphics**: OpenGL 4.5+ / Vulkan (future)
- **Window/Input**: GLFW
- **Math**: GLM
- **Audio**: OpenAL Soft / FMOD
- **Dependencies**: vcpkg package manager
- **Build System**: CMake
- **Testing**: GoogleTest

## 📋 Development Phases

### Phase 1: Foundation (Weeks 1-2)
- [x] Project setup & CMake configuration  
- [ ] Core engine architecture
- [ ] Basic OpenGL context & window
- [ ] Shader system implementation
- [ ] Camera & input system

### Phase 2: Rendering (Weeks 3-4)
- [ ] Chunk-based world rendering
- [ ] Texture atlas system
- [ ] Basic lighting model
- [ ] Frustum culling optimization

### Phase 3: World Generation (Weeks 5-6)
- [ ] Perlin noise terrain generation
- [ ] Biome system
- [ ] Cave generation (convert WASM to C++)
- [ ] Chunk loading/unloading

### Phase 4: Physics & Interaction (Weeks 7-8)
- [ ] Block collision detection
- [ ] Player physics & movement
- [ ] Block placement/breaking
- [ ] Item pickup system

### Phase 5: Game Systems (Weeks 9-10)
- [ ] Inventory & crafting
- [ ] UI rendering system  
- [ ] Audio integration
- [ ] World persistence

### Phase 6: Polish & Optimization (Weeks 11-12)
- [ ] Performance optimization
- [ ] Memory management
- [ ] Multi-threading
- [ ] Final testing & debugging

## 🎮 Target Performance

- **60+ FPS** at 1920x1080 resolution
- **16+ chunk** render distance  
- **<4GB RAM** usage for large worlds
- **<100ms** chunk generation time
- **RTX 2070 SUPER** reference hardware

## 📊 Source Material Analysis

**MineKhan Statistics:**
- **Total JavaScript Code**: ~200KB (4,665+ lines)
- **Key Systems**: 15+ modular JavaScript files
- **Rendering**: WebGL with custom shaders
- **Performance**: Optimized chunk system with WASM cave generation
- **Features**: Nearly feature-complete Minecraft clone

## 🛠️ Build Instructions

```bash
# Prerequisites: Visual Studio 2022, vcpkg, CMake 3.20+

# Clone repository
git clone <repository-url>
cd CppCraft

# Install dependencies via vcpkg
vcpkg install glfw3 glm glad openal-soft stb

# Build project
mkdir build && cd build
cmake .. -DCMAKE_TOOLCHAIN_FILE=path/to/vcpkg.cmake
cmake --build . --config Release

# Run engine
./CppCraft.exe
```

## 🎯 Success Criteria

- [ ] **Functional Parity**: All MineKhan features working in C++
- [ ] **Performance**: 2x+ faster than browser version
- [ ] **Scalability**: Support larger worlds than JavaScript version
- [ ] **Extensibility**: Clean C++ architecture for future features
- [ ] **Cross-Platform**: Windows, Linux, macOS support

## 📄 License

MIT License - Convert, modify, and distribute freely.

## 🤝 Contributing

Contributions welcome! See [PROGRESS.md](PROGRESS.md) for current development status.

---

*Converting the web's best Minecraft clone to native C++ performance* 🚀 