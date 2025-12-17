# 🎯 实战案例：30 分钟做一个 Todo App

> 难度：⭐ 入门 | 技术栈：HTML/CSS/JS | 耗时：30 分钟

---

## 最终效果

<!-- TODO: 添加 GIF 演示 -->
一个简洁的待办事项应用，支持：
- ✅ 添加任务
- ✅ 完成/取消完成
- ✅ 删除任务
- ✅ 本地存储（刷新不丢失）

---

## 第 1 步：启动对话

复制以下提示词，粘贴到 [Claude](https://claude.ai/) 或 [ChatGPT](https://chatgpt.com/)：

```
你是一个专业的前端开发助手。我想用 Vibe Coding 的方式做一个 Todo App。

项目要求：
- 纯 HTML/CSS/JS，不用任何框架
- 单文件实现（一个 index.html）
- 功能：添加任务、完成任务、删除任务
- 数据存到 localStorage，刷新不丢失
- 界面简洁美观，有动画效果

请直接给我完整代码，我复制到 index.html 就能运行。
```

---

## 第 2 步：获取代码

AI 会给你一个完整的 `index.html` 文件，大约 150-200 行代码。

**示例代码结构**：
```html
<!DOCTYPE html>
<html>
<head>
    <title>Todo App</title>
    <style>
        /* 样式代码 */
    </style>
</head>
<body>
    <div class="container">
        <h1>📝 我的待办</h1>
        <input type="text" id="input" placeholder="添加新任务...">
        <ul id="list"></ul>
    </div>
    <script>
        // JS 代码
    </script>
</body>
</html>
```

---

## 第 3 步：运行测试

1. 新建文件 `index.html`
2. 粘贴 AI 给的代码
3. 双击打开，或用 VS Code Live Server

---

## 第 4 步：迭代优化

不满意？继续对话：

```
请帮我优化：
1. 添加深色模式切换
2. 任务支持拖拽排序
3. 添加任务分类功能
```

---

## 踩坑记录

| 问题 | 解决方案 |
|:---|:---|
| localStorage 报错 | 用浏览器打开，不要直接双击 file:// |
| 样式不生效 | 检查 CSS 是否在 `<style>` 标签内 |
| 刷新数据丢失 | 检查 localStorage.setItem 是否正确调用 |

---

## 进阶挑战

完成基础版后，尝试：

1. **添加截止日期** - 支持设置 deadline
2. **添加优先级** - 高/中/低三档
3. **添加搜索** - 快速查找任务
4. **PWA 化** - 可安装到桌面

---

## 学到了什么

- ✅ Vibe Coding 基本流程：描述需求 → 获取代码 → 运行测试 → 迭代优化
- ✅ 单文件 Web 应用结构
- ✅ localStorage 本地存储
- ✅ 如何与 AI 迭代优化代码

---

**下一个案例**：[个人博客](./02-blog.md) →
