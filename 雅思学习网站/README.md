# 雅思学习网站

中英双语词汇、随机分组、拼写与听写、音频播放及复习进度。包含 2,412 条牛津 A2–B2 词条及 196 条主题词条；已移除 A1。

## 本地运行

需要 Node.js 20 或更新版本，无第三方运行依赖。

```sh
npm test
npm run build
npm start
```

打开 http://localhost:4173 。本地预览可用词汇和设备本地进度；云端同步及 AI 需要托管环境。

## 部署

Worker 入口为 worker/index.js，构建产物为 dist/server/index.js。配置 D1 绑定 DB 并按顺序执行 drizzle 下 SQL 迁移。部署到新的 Sites 项目后，在 .openai/hosting.json 写入新项目返回的 project_id；仓库不包含原站点身份。

DEEPSEEK_API_KEY 必须配置为服务端 secret；DEEPSEEK_MODEL 为可选模型设置。不要把密钥写入前端或提交到 Git。托管身份由可信平台注入 oai-authenticated-user-id；自行部署必须实现可信身份认证并移除客户端伪造的身份头。

匿名用户使用本地进度；登录后可同步个人进度及使用 AI（每用户每日 20 次）。公开站点关闭在线内容写入，内容更新通过源码发布。

## 音频与词表

在线音频通过有道词典链接提供，也支持设备语音；不包含音频录音文件。可调整播放速度。词条顺序随机，恢复未完成会话时保留原顺序。拼写/听写错误后按回车或“再来一次”隐藏答案，完成当前词后继续。

见 THIRD_PARTY.md 了解第三方词表与音频说明。学习词库不是雅思官方指定词表。
