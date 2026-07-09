<div align="center">
   <img width="1782" height="348" alt="image" src="https://github.com/user-attachments/assets/03ade2af-88c0-4c0d-be1e-3a50fe2cd697" />
</div>


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

### 3. 配置 Qwen API Key

本项目的客户端示例使用通义千问 Qwen 的 OpenAI-compatible 接口。运行前需要先去 Qwen/阿里云百炼官网申请 API Key，然后替换代码里的占位符。

1. 打开阿里云百炼 API Key 页面：https://bailian.console.aliyun.com/?apiKey=1#/api-key
2. 登录阿里云账号，按页面提示创建 API Key。
3. 打开 `mcp_client.py`，把下面这一行中的占位内容替换成你自己的 API Key：
   ```python
   api_key="sk-换成自己的API KEY"
   ```
4. 替换后示例：
   ```python
   api_key="你的 Qwen API Key"
   ```

注意：API Key 是私密凭证，不要把自己的真实 API Key 上传到公开仓库，也不要发到截图、群聊或文章里。

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
   确认已经将 `mcp_client.py` 中的 Qwen API Key 占位符替换为自己的 API Key，之后打开新的终端窗口，执行客户端脚本，客户端会与服务端建立通信并发起工具调用：
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

