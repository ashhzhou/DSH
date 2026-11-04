# DSH

这个仓库是 [`dsh-superagent`](https://github.com/deepseek-ai/dsh-superagent-prototype) 的试点仓库：
一个常驻的编码智能体（GitHub 账号 [`@rapeon-dsh`](https://github.com/rapeon-dsh)）在这里接需求、开工单、提 PR。

## 怎么让它干活

在 Issue 或评论里直接 @ 它，并写清要什么：

```
@rapeon-dsh 把 README 的「怎么让它干活」一节改成英文
```

- 只有白名单里的账号（目前仅 `@ashhzhou`）发出的明确请求才会被受理
- 它自己判断要不要接、怎么拆、做到什么程度；不需要事先建任务清单
- 它会在自己的 Session 和独立工作目录里干活，完成后在**原对话**里回复，通常附一个 PR
- 分支名以 `agent/` 开头；PR 由人合并，它不会自行合并

## 约定

- 一个请求一个工单：请把「要什么」和「验收标准」写在同一条消息里
- 需要设计取舍的改动，它会停下来提问，而不是自行拍板
- 它说的话代表这个仓库，写错了请在 Issue 里纠正，或直接改 `.dsh/` 下的提示词（如已配置）

## 本地环境

试点部署在 Windows 上，`dsh-superagent` 的面板在 `http://127.0.0.1:3082`，
启停脚本见部署机的 `dsh-superagent/scripts/dsh-superagent.ps1`。
