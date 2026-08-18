# Science DSH Plugins Collection

这个仓库收集了我认为重要的 DSH 相关项目。

## 项目列表

- [dsh-plugins](https://github.com/CiicDong/dsh-plugins) - DSH 插件集合
- [dsh-routing-suite](./dsh-routing-suite) - DSH 路由套件（已内置，包含 injector 和 preset）
- [dsh-genui](https://github.com/omdsh-dev/dsh-genui) - GenUI 生成式 UI 插件
- [dsh-univer-office](./dsh-univer-office) - Univer Office 集成插件（已内置）
- [dsh-mcp-manage](https://github.com/wuhobin/dsh-mcp-manage) - MCP 管理插件

## 安装说明

### 重要提示

**必须进入各插件目录使用提供的安装脚本或按照其 README 说明进行安装。**

### dsh-genui

进入目录，使用安装脚本：

```bash
cd dsh-genui
bash scripts/install.sh
```

### dsh-univer-office

该插件需要先构建再安装：

```bash
cd dsh-univer-office
pnpm install
pnpm run build

# 使用 link 模式安装
dsh plugin --profile web add link:$PWD
```

## 克隆仓库

`dsh-routing-suite` 和 `dsh-univer-office` 已作为普通目录收录；其他项目仍使用子模块。克隆完整仓库：

```bash
git clone --recurse-submodules https://github.com/CiicDong/science-dsh-plugins.git
```

或者先克隆主仓库，再初始化子模块：

```bash
git clone https://github.com/CiicDong/science-dsh-plugins.git
cd science-dsh-plugins
git submodule update --init --recursive
```

## 更新其余子模块

```bash
git submodule update --remote --merge
```
