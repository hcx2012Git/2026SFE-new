# 2026年春节编辑松联络员审核工具

这是一个（半）自动化机器人，用于统计参与者在 2026 年春节编辑松中的贡献，并自动更新排行榜。

代码衍生自HYYY_bot（仓库：https://github.com/ZoruaFox/2026SFE ）和 https://github.com/hcx2012Git/tools-for-26SFE 。

## 功能

1.  **自动统计**：扫描用户贡献页，统计通过的条目数及积分。
2.  **更新提示板**：更新用户个人贡献页顶部的 `{{mbox}}` 状态。
3.  **排行榜管理**：自动区分“熟练编者”与“新星编者”，并更新总排行榜。

## 运行环境

*   Node.js 18+
*   MediaWiki OAuth 2.0 权限

## 安装与配置

1.  安装依赖：
    ```bash
    pnpm install
    ```

2.  配置环境变量：
    复制 `.env.example` 为 `.env` 并填写配置：
    ```bash
    cp .env.example .env
    ```
    *   `OAUTH2_CLIENT_ID`: OAuth 2.0 客户端 ID
    *   `OAUTH2_CLIENT_SECRET`: OAuth 2.0 客户端密钥

## 运行

### 本地运行
#### 更新排行榜和总得分
```bash
node HYYY_bot.js
```
#### 获取待审核列表
```bash
node get_pending_list.js
```

#### 审核工具（服务器模式）
运行（需要同意防火墙）
```bash
node website.js
```

访问http://localhost:2026/ ，即可。


## 许可协议

本项目采用 [MIT License](LICENSE) 开源许可协议。

其中图标（即[favicon.ico](public/favicon.ico)）源自[求闻百科](https://www.qiuwenbaike.cn/wiki/File:%E2%80%9C%E6%B1%82%E2%80%9D%E7%BD%91%E7%AB%99%E5%9B%BE%E6%A0%87%EF%BC%88%E9%80%8F%E6%98%8E%E8%83%8C%E6%99%AF%EF%BC%9B2024%E7%89%88%EF%BC%9B%E7%BA%A2%E8%89%B2%E6%96%B9%E6%8B%AC%E5%8F%B7%EF%BC%89.svg)，署名求闻百科技术团队，采用[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.zh)授权

## 声明

本仓库代码包含 GitHub Copilot、通义灵码 生成内容。
