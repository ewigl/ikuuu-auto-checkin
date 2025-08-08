## iKuuu 定时自动签到

> 利用 Github Actions 实现自动签到，支持多账户，支持 Telegram 通知。

[![IKUUU-Auto-Checkin](https://github.com/ewigl/ikuuu-auto-checkin/actions/workflows/Checkin.yml/badge.svg)](https://github.com/ewigl/ikuuu-auto-checkin/actions/workflows/Checkin.yml)

### 仓库 Secrets

- **ACCOUNTS**：账户信息，**多个**账户配置示例如下。推荐使用 [JSON 格式化工具](https://jsoneditoronline.org/) 进行编辑以避免格式出错。

  ```json
  [
    {
      "name": "这里填写账户备注",
      "email": "这里填写邮箱",
      "passwd": "这里填写密码"
    },
    {
      "name": "这里填写账户备注",
      "email": "这里填写邮箱",
      "passwd": "这里填写密码"
    }
  ]
  ```

- **TELEGRAM_TOKEN**: （可选）Telegram 通知的 Bot Token。
- **TELEGRAM_TO**: （可选）Telegram 通知的 Chat ID。

### 仓库 Variables

- **HOST**: （可选）iKuuu 的域名，不设置时默认为 `ikuuu.de`。

### 使用方法

1. Fork 此仓库。
2. 在 fork 后的仓库中启用 Actions。
3. 配置仓库 Secrets 和 Variables。

详细文档: https://ewigl.github.io/notes/posts/programming/github-actions/

### 注意事项

根据 [Github 的政策](https://docs.github.com/zh/actions/managing-workflow-runs-and-deployments/managing-workflow-runs/disabling-and-enabling-a-workflow?tool=webui)，当 60 天内未发生仓库活动时，将自动禁用定时 Workflow。需要再次手动启用。
