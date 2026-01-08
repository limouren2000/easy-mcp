# easy-mcp

## 介绍
本项目基于 [Model Context Protocol (MCP)](https://modelcontextprotocol.io/docs/getting-started/intro) 官方示例，演示如何通过 MCP 协议实现 Agent 工具调用的核心流程。项目包含完整的服务端和客户端实现，采用 Stdio 通信模式，适合新手快速理解 MCP 协议的基本使用方式。

## 项目结构
```
easy-mcp/
├── mcp_server.py    # MCP 服务端核心逻辑，提供工具调用能力
├── mcp_client.py    # MCP 客户端实现（Stdio 通信模式），发起工具调用请求
├── requirements.txt # 项目依赖清单
└── README.md        # 项目说明文档
```

## 环境准备
### 1. 基础环境要求
- Python 3.8+
- pip（Python 包管理工具）

### 2. 安装依赖
在项目根目录下执行以下命令安装所需依赖：
```bash
pip install -r requirements.txt
```

## 快速开始
### 执行步骤（按顺序执行）

1. **启动 MCP 服务端**
   在终端执行服务端脚本，服务端会持续运行并等待客户端连接：
   ```bash
   python mcp_server.py
   ```
   <div align="center">
     <img width="1280" height="740" alt="启动MCP服务端" src="https://github.com/user-attachments/assets/ac92cca0-dc17-4f8b-904c-0d11b8da42d7" />
   </div>

2. **启动 MCP 客户端**
   更改代码中的 API key 为你自己的 Qwen API，之后打开新的终端窗口，执行客户端脚本，客户端会与服务端建立通信并发起工具调用：
   ```bash
   python mcp_client.py
   ```
   <div align="center">
     <img width="1280" height="608" alt="启动MCP客户端" src="https://github.com/user-attachments/assets/b593e306-525e-4fa3-b2f4-0a1275e4c643" />
   </div>

3. **开始使用你的 Agent**  
   输入“洛杉矶的天气怎么样？”
   <div align="center">
     <img width="1280" height="722" alt="使用Agent工具调用" src="https://github.com/user-attachments/assets/e1a027d0-87b0-4aca-bff2-dacd898ba7b4" />
   </div>

