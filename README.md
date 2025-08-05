# pytest-homeassistant-custom-component-fixed

[English](#english) | [中文](#中文)

## English

### Overview

This is a fork of pytest-homeassistant-custom-component that provides enhanced compatibility for macOS ARM64 environments and supports multiple Home Assistant versions through optimized branch structure.

**Originally created for [LifeSmart Integration](https://github.com/MapleEve/lifesmart-HACS-for-hass) - A comprehensive Home Assistant integration for LifeSmart smart home devices!**

![HA core versions](https://img.shields.io/static/v1?label=HA+core+versions&message=2022.10.0%20%7C%202023.6.0&labelColor=blue)

### Branch Structure

| Branch | Home Assistant Version | Python Version | Purpose |
|--------|----------------------|----------------|---------|
| `macos-fix-branch` | 2023.6.0 | 3.11 | macOS ARM64 compatibility for Python 3.11 environments |
| `py310-fix-branch` | 2022.10.0 | 3.10 | macOS ARM64 compatibility for Python 3.10 environments |

### Key Improvements

- **macOS ARM64 lru-dict compatibility**: Enhanced lru-dict dependency management
- **Multi-version support**: Separate branches for different HA/Python combinations
- **Dependency optimization**: Resolved conflicts with forked Home Assistant versions
- **Enhanced testing**: Improved compatibility with custom testing environments

### Usage

#### For Python 3.11 + HA 2023.6.0:
```bash
pip install git+https://github.com/MapleEve/pytest-homeassistant-custom-component-fixed.git@macos-fix-branch
```

#### For Python 3.10 + HA 2022.10.0:
```bash
pip install git+https://github.com/MapleEve/pytest-homeassistant-custom-component-fixed.git@py310-fix-branch
```

### Companion Repository

This fork works in conjunction with:
- [homeassistant-lru-dict-macos-fix](https://github.com/MapleEve/homeassistant-lru-dict-macos-fix)

### 🏠 Featured Project: LifeSmart Integration

This fork was specifically created to support comprehensive testing of the **[LifeSmart Integration for Home Assistant](https://github.com/MapleEve/lifesmart-HACS-for-hass)**.

#### What is LifeSmart Integration?
A powerful Home Assistant integration that brings LifeSmart smart home ecosystem to your Home Assistant setup:

- **🔌 Comprehensive Device Support**: Lights, switches, sensors, climate control, covers, and more
- **☁️ Multi-Connection Methods**: Local TCP, WebSocket, and OpenAPI support
- **🎯 Advanced Features**: Scene management, real-time status updates, and device discovery
- **🧪 Robust Testing**: Multi-environment CI/CD testing across HA versions 2022.10.0 to latest
- **📱 Easy Installation**: Available through HACS (Home Assistant Community Store)

**[⭐ Star the LifeSmart Integration Repository](https://github.com/MapleEve/lifesmart-HACS-for-hass)** to stay updated with the latest features and improvements!

### Testing Usage

* All pytest fixtures can be used as normal, like `hass`
* For helpers:
  * home-assistant/core native test: `from tests.common import MockConfigEntry`
  * custom component test: `from pytest_homeassistant_custom_component.common import MockConfigEntry`
* If your integration is inside a `custom_components` folder, a `custom_components/__init__.py` file or changes to `sys.path` may be required.
* `enable_custom_integrations` fixture is required (versions >=2021.6.0b0)
* If using `load_fixture`, the files need to be in a `fixtures` folder colocated with the tests.

### Original Repository

Based on [pytest-homeassistant-custom-component](https://github.com/MatthewFlamm/pytest-homeassistant-custom-component)

---

## 中文

### 概述

这是 pytest-homeassistant-custom-component 的一个分支，为 macOS ARM64 环境提供增强的兼容性，并通过优化的分支结构支持多个 Home Assistant 版本。

**最初为 [LifeSmart 集成](https://github.com/MapleEve/lifesmart-HACS-for-hass) 而创建 - 一个全面的 Home Assistant LifeSmart 智能家居设备集成！**

![HA 核心版本](https://img.shields.io/static/v1?label=HA+core+versions&message=2022.10.0%20%7C%202023.6.0&labelColor=blue)

### 分支结构

| 分支 | Home Assistant 版本 | Python 版本 | 用途 |
|------|-------------------|-------------|------|
| `macos-fix-branch` | 2023.6.0 | 3.11 | Python 3.11 环境的 macOS ARM64 兼容性 |
| `py310-fix-branch` | 2022.10.0 | 3.10 | Python 3.10 环境的 macOS ARM64 兼容性 |

### 主要改进

- **macOS ARM64 lru-dict 兼容性**: 增强的 lru-dict 依赖管理
- **多版本支持**: 为不同 HA/Python 组合提供独立分支
- **依赖优化**: 解决与 fork 版本 Home Assistant 的冲突
- **增强测试**: 提高与自定义测试环境的兼容性

### 使用方法

#### Python 3.11 + HA 2023.6.0:
```bash
pip install git+https://github.com/MapleEve/pytest-homeassistant-custom-component-fixed.git@macos-fix-branch
```

#### Python 3.10 + HA 2022.10.0:
```bash
pip install git+https://github.com/MapleEve/pytest-homeassistant-custom-component-fixed.git@py310-fix-branch
```

### 配套仓库

此分支与以下仓库配合使用:
- [homeassistant-lru-dict-macos-fix](https://github.com/MapleEve/homeassistant-lru-dict-macos-fix)

### 🏠 重点项目：LifeSmart 集成

此分支专门为支持 **[LifeSmart Home Assistant 集成](https://github.com/MapleEve/lifesmart-HACS-for-hass)** 的全面测试而创建。

#### 什么是 LifeSmart 集成？
一个强大的 Home Assistant 集成，将 LifeSmart 智能家居生态系统带入您的 Home Assistant 设置：

- **🔌 全面的设备支持**: 灯光、开关、传感器、气候控制、窗帘等
- **☁️ 多种连接方式**: 支持本地 TCP、WebSocket 和 OpenAPI
- **🎯 高级功能**: 场景管理、实时状态更新和设备发现
- **🧪 健壮的测试**: 跨 HA 版本 2022.10.0 到最新版本的多环境 CI/CD 测试
- **📱 简易安装**: 通过 HACS (Home Assistant Community Store) 可用

**[⭐ 为 LifeSmart 集成仓库点星标](https://github.com/MapleEve/lifesmart-HACS-for-hass)** 以获取最新功能和改进！

### 测试使用

* 所有 pytest fixtures 都可以正常使用，比如 `hass`
* 对于 helpers:
  * home-assistant/core 原生测试: `from tests.common import MockConfigEntry`
  * 自定义组件测试: `from pytest_homeassistant_custom_component.common import MockConfigEntry`
* 如果您的集成在 `custom_components` 文件夹内，可能需要 `custom_components/__init__.py` 文件或修改 `sys.path`
* 需要 `enable_custom_integrations` fixture (版本 >=2021.6.0b0)
* 如果使用 `load_fixture`，文件需要在与测试并排的 `fixtures` 文件夹中

### 原始仓库

基于 [pytest-homeassistant-custom-component](https://github.com/MatthewFlamm/pytest-homeassistant-custom-component)

---

### Technical Details | 技术细节

#### Changes Made | 所做更改

1. **lru-dict Compatibility Enhancement | lru-dict 兼容性增强**
   - Updated to lru-dict==1.3.0 for macOS ARM64 compatibility
   - Resolved dependency conflicts with forked Home Assistant versions

2. **Dependency Management | 依赖管理**
   - `py310-fix-branch`: Removed hardcoded homeassistant==2022.10.0 dependency
   - `macos-fix-branch`: Compatible with HA 2023.6.0 fork

3. **Multi-Environment Testing Support | 多环境测试支持**
   - Optimized for LifeSmart integration testing across 5 HA versions
   - Enhanced compatibility with custom testing workflows

#### Compatibility Matrix | 兼容性矩阵

| Environment | Branch | HA Fork Branch | lru-dict Version | Status |
|-------------|--------|----------------|------------------|--------|
| macOS ARM64 + Python 3.10 | `py310-fix-branch` | `py310-fix-branch` | 1.3.0 | ✅ Working |
| macOS ARM64 + Python 3.11 | `macos-fix-branch` | `macos-fix-branch` | 1.3.0 | ✅ Working |

#### Used by LifeSmart Integration Testing | 用于 LifeSmart 集成测试

This dual-fork solution enables comprehensive testing of the LifeSmart integration:
- **Unit Tests**: Individual component functionality
- **Integration Tests**: Cross-component interactions
- **Platform Tests**: Device-specific testing (lights, switches, sensors, etc.)
- **Mock Architecture**: Precise mocking to prevent thread leakage while preserving business logic

此双分支解决方案支持 LifeSmart 集成的全面测试：
- **单元测试**: 单个组件功能
- **集成测试**: 跨组件交互
- **平台测试**: 设备特定测试（灯光、开关、传感器等）
- **Mock 架构**: 精确 mock 防止线程泄漏同时保留业务逻辑

### Contributing | 贡献

This fork is specifically designed for LifeSmart integration testing. For general pytest-homeassistant-custom-component contributions, please use the [original repository](https://github.com/MatthewFlamm/pytest-homeassistant-custom-component).

If you're interested in LifeSmart devices and Home Assistant, check out the **[LifeSmart Integration project](https://github.com/MapleEve/lifesmart-HACS-for-hass)**!

此分支专为 LifeSmart 集成测试设计。如需对 pytest-homeassistant-custom-component 进行一般性贡献，请使用[原始仓库](https://github.com/MatthewFlamm/pytest-homeassistant-custom-component)。

如果您对 LifeSmart 设备和 Home Assistant 感兴趣，请查看 **[LifeSmart 集成项目](https://github.com/MapleEve/lifesmart-HACS-for-hass)**！