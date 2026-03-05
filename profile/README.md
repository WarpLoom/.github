# WarpLoom

**Open-source, free TypeScript-first development framework.**

WarpLoom is building toward an engine-agnostic development platform where you write your logic once in TypeScript and deploy across multiple engines. Currently focused on Unity with PuerTS integration, the project is being built from the ground up—each layer adding more engine-agnostic abstractions.

The long-term vision includes engine-specific bridges for Unity, Godot, Unreal, and others, with common high-level JavaScript frameworks that work seamlessly across all of them. Write your logic in TypeScript with modern web development practices, then choose your engine.

## Current Features (Unity)

- **TypeScript Logic**: Write your scripts in TypeScript with full type safety and modern JavaScript features
- **JSBehaviour**: MonoBehaviour lifecycle host that forwards Unity callbacks to TypeScript
- **DOTS/ECS Support**: Bridge between Unity's Data-Oriented Technology Stack and JavaScript runtime
- **GameObject/Behaviour Abstraction**: High-level API that makes DOTS feel like traditional Unity development
- **Seamless C# Integration**: Full access to Unity's C# APIs through PuerTS

## Architecture Vision

WarpLoom is being developed in layers, each adding more engine-agnostic capabilities:

1. **Engine Bridges** (Current: Unity) - Low-level bindings to specific engines
2. **Unified APIs** (In Progress) - Common abstractions that work across engines
3. **Framework Layer** (Planned) - High-level, engine-agnostic development frameworks
4. **Tooling** (Planned) - Shared development tools, debugging, and hot-reload across all engines

As each layer matures, developers gain more portability and can share code between different engine targets.

## Project Structure

WarpLoom consists of several repositories:

### Core Libraries

- **[unity-core](https://github.com/WarpLoom/unity-core)** - Unity Package Manager (UPM) library containing both C# runtime and TypeScript APIs. The foundation of the WarpLoom architecture.

- **[unity-dots-behaviours-ts](https://github.com/WarpLoom/unity-dots-behaviours-ts)** - TypeScript extension that provides GameObject/MonoBehaviour-style API for working with Unity DOTS/ECS, making ECS development feel familiar.

### Development & Testing

- **[unity-dev](https://github.com/WarpLoom/unity-dev)** - Sandbox Unity project for developing and testing the WarpLoom framework.

- **[webium-dev](https://github.com/WarpLoom/webium-dev)** - Development project for Webium (UI framework integration).

## Getting Started

Add `unity-core` to your Unity project's `Packages/manifest.json`:

```json
{
  "dependencies": {
    "com.warploom.core": "https://github.com/WarpLoom/unity-core.git"
  }
}
```

Install the TypeScript runtime:

```bash
npm install @warploom/unity-core
```

## Requirements

- Unity 2021.3+
- PuerTS (`com.tencent.puerts.core`)
- Node.js and npm for TypeScript development

## Roadmap

### Near Term (Unity)
- Input system integration
- UI framework support
- Additional DOTS features
- Enhanced tooling and debugging

### Long Term (Multi-Engine)
- Godot bridge and integration
- Unreal Engine bridge
- Engine-agnostic core frameworks
- Unified input, UI, and ECS abstractions
- Cross-engine project templates and tooling

## License

WarpLoom is open source and free to use under the MIT License. See individual repository LICENSE files for details.

## Contributing

Contributions are welcome! This is an open-source project maintained by the community.
