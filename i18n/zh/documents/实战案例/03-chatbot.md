# 🤖 实战案例：1 小时做一个 AI 聊天机器人

> 难度：⭐⭐ 初级 | 技术栈：Python/FastAPI | 耗时：1 小时

---

## 最终效果

<!-- TODO: 添加 GIF 演示 -->
一个简单的 AI 聊天机器人，支持：
- ✅ Web 界面对话
- ✅ 接入 OpenAI/Claude API
- ✅ 流式输出（打字机效果）
- ✅ 对话历史记录

---

## 前置条件

- Python 3.8+
- OpenAI API Key（或其他 LLM API）

---

## 第 1 步：启动对话

复制以下提示词：

```
你是一个 Python 后端开发助手。我想用 Vibe Coding 的方式做一个 AI 聊天机器人。

项目要求：
- 后端：FastAPI
- 前端：简单 HTML 页面（内嵌在 FastAPI 中）
- 功能：用户输入问题，调用 OpenAI API 返回回答
- 支持流式输出（SSE）
- 界面简洁，类似 ChatGPT

请给我：
1. 项目结构
2. requirements.txt
3. 完整代码
4. 运行命令

我的 OpenAI API Key 会通过环境变量 OPENAI_API_KEY 传入。
```

---

## 第 2 步：创建项目

AI 会给你类似这样的结构：

```
chatbot/
├── main.py          # FastAPI 主程序
├── requirements.txt # 依赖
└── .env            # API Key（自己创建）
```

**requirements.txt**：
```
fastapi
uvicorn
openai
python-dotenv
sse-starlette
```

---

## 第 3 步：运行

```bash
# 安装依赖
pip install -r requirements.txt

# 设置 API Key
export OPENAI_API_KEY="sk-xxx"

# 启动服务
uvicorn main:app --reload
```

打开 http://localhost:8000 即可使用。

---

## 第 4 步：迭代优化

```
请帮我添加：
1. 对话历史保存到文件
2. 支持切换不同模型（GPT-4/GPT-3.5）
3. 添加系统提示词设置
4. 支持 Markdown 渲染
```

---

## 踩坑记录

| 问题 | 解决方案 |
|:---|:---|
| API Key 无效 | 检查环境变量是否正确设置 |
| 跨域错误 | FastAPI 添加 CORS 中间件 |
| 流式输出不工作 | 检查 SSE 配置，前端用 EventSource |
| 中文乱码 | 确保 response 设置 `charset=utf-8` |

---

## 进阶挑战

1. **添加 RAG** - 让机器人能读取本地文档
2. **多轮对话** - 保持上下文记忆
3. **部署上线** - 部署到 Vercel/Railway
4. **接入微信** - 做成微信机器人

---

## 学到了什么

- ✅ FastAPI 基础用法
- ✅ OpenAI API 调用
- ✅ SSE 流式输出
- ✅ 前后端一体化开发

---

← [Todo App](./01-todo-app.md) | **下一个案例**：[全栈 SaaS](./04-saas.md) →
