# RisuAI 懒猫应用

本仓库将 [RisuAI](https://github.com/kwaroran/Risuai) 打包为懒猫应用。RisuAI 是一款 AI 角色扮演聊天客户端，支持角色卡、多种模型服务、世界书、插件和丰富的对话控制功能。

## 使用方法

从懒猫启动器打开 RisuAI，然后在 RisuAI 设置中选择模型服务并填写 API 地址和密钥。模型是否可用、账号要求和 API 费用由所选服务商决定。

RisuAI 可能会将模型 API 密钥保存在应用数据中，请只允许可信用户和设备访问该应用。

## 数据持久化

上游的 `/app/save` 目录映射到 `/lzcapp/var/save`。聊天记录、角色卡、设置和其他 RisuAI 数据在应用重启和升级后会保留。重新安装或进行大版本升级前，建议备份懒猫应用数据。

## 镜像与发布

初始版本使用 `ghcr.1ms.run/kwaroran/risuai:v2026.6.214` 加速拉取镜像。GitHub Action 从 `ghcr.io/kwaroran/risuai` 发现新版本，严格校验源镜像与加速镜像的 `linux/amd64` 摘要一致，构建版本化 LPK，并且只发布到喵喵私有商店。

## 相关链接

- [RisuAI 源码](https://github.com/kwaroran/Risuai)
- [RisuAI 官网](https://risuai.net)
- [懒猫应用打包仓库](https://github.com/lazycat-contrib/risuai-lzcapp)
