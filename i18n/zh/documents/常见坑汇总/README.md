# 🕳️ 常见坑汇总

> Vibe Coding 过程中的常见问题和解决方案

---

<details open>
<summary><strong>🤖 AI 对话相关</strong></summary>

| 问题 | 原因 | 解决方案 |
|:---|:---|:---|
| AI 生成的代码跑不起来 | 上下文不足 | 提供完整错误信息，说明运行环境 |
| AI 反复修改同一个问题 | 陷入循环 | 换个思路描述，或开新对话 |
| AI 幻觉，编造不存在的 API | 模型知识过时 | 提供官方文档链接，让 AI 参考 |
| 代码越改越乱 | 没有规划 | 先让 AI 出方案，确认后再写代码 |
| AI 不理解我的需求 | 描述模糊 | 用具体例子说明，给输入输出示例 |

</details>

---

<details open>
<summary><strong>🔧 环境配置相关</strong></summary>

| 问题 | 原因 | 解决方案 |
|:---|:---|:---|
| npm install 报错 | 网络问题 | 换源：`npm config set registry https://registry.npmmirror.com` |
| pip install 超时 | 网络问题 | 换源：`pip install -i https://pypi.tuna.tsinghua.edu.cn/simple` |
| 命令找不到 | 环境变量没配 | 检查 PATH，重启终端 |
| 端口被占用 | 上次没关干净 | `lsof -i :端口号` 找到进程 kill 掉 |
| 权限不足 | Linux/Mac 权限 | `chmod +x` 或 `sudo` |

</details>

---

<details open>
<summary><strong>🌐 网络相关</strong></summary>

| 问题 | 原因 | 解决方案 |
|:---|:---|:---|
| GitHub 访问慢/超时 | 网络限制 | 配置代理，参考 [网络环境配置](../从零开始vibecoding/01-网络环境配置.md) |
| API 调用失败 | 网络/Key 问题 | 检查代理、API Key 是否有效 |
| 终端不走代理 | 代理配置不全 | 设置 `http_proxy` 和 `https_proxy` 环境变量 |
| SSL 证书错误 | 代理/时间问题 | 检查系统时间，或临时关闭 SSL 验证 |

</details>

---

<details open>
<summary><strong>📝 代码相关</strong></summary>

| 问题 | 原因 | 解决方案 |
|:---|:---|:---|
| 代码文件太大，AI 处理不了 | 超出上下文 | 拆分文件，只给 AI 相关部分 |
| 改了代码没生效 | 缓存/没保存 | 清缓存、确认保存、重启服务 |
| 合并代码冲突 | Git 冲突 | 让 AI 帮你解决：贴出冲突内容 |
| 依赖版本冲突 | 版本不兼容 | 指定版本号，或用虚拟环境隔离 |

</details>

---

<details>
<summary><strong>🎯 Claude Code / Cursor 相关</strong></summary>

| 问题 | 原因 | 解决方案 |
|:---|:---|:---|
| Claude Code 连不上 | 网络/认证 | 检查代理，重新 `claude login` |
| Cursor 补全很慢 | 网络延迟 | 检查代理配置 |
| 额度用完了 | 免费额度有限 | 换账号或升级付费 |
| 规则文件不生效 | 路径/格式错误 | 检查 `.cursorrules` 或 `CLAUDE.md` 位置 |

</details>

---

<details>
<summary><strong>🚀 部署相关</strong></summary>

| 问题 | 原因 | 解决方案 |
|:---|:---|:---|
| 本地能跑，部署失败 | 环境差异 | 检查 Node/Python 版本，环境变量 |
| 构建超时 | 项目太大 | 优化依赖，增加构建时间限制 |
| 环境变量没生效 | 没配置 | 在部署平台设置环境变量 |
| CORS 跨域错误 | 后端没配置 | 添加 CORS 中间件 |

</details>

---

## 💡 通用排查思路

1. **看错误信息** - 完整复制给 AI
2. **最小复现** - 找到最简单能复现问题的代码
3. **二分法** - 注释一半代码，定位问题范围
4. **换环境** - 换浏览器/终端/设备试试
5. **重启大法** - 重启服务/编辑器/电脑

---

## 📝 贡献

遇到新坑？欢迎 PR 补充！
