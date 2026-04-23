# AGENTS 项目全局指引
适配：C# WPF / .NET8
用途：统一项目规范、架构、目录、协作标准

## 一、项目介绍
- 技术栈：C# 、.NET 8 、WPF
- 架构模式：MVVM
- 开发工具：Visual Studio 2022
- 项目类型：Windows 桌面客户端

## 二、目录结构
├── AGENTS.md
├── README.md
├── src/
│ ├── Views/ # 窗口、页面
│ ├── ViewModels/ # MVVM 逻辑层
│ ├── Models/ # 数据实体
│ ├── Controls/ # 自定义控件
│ ├── Common/ # 工具类、公共方法
│ ├── Converters/ # XAML 转换器
│ ├── Commands/ # 自定义命令
│ ├── Services/ # 数据库、网络、业务服务
│ ├── Assets/ # 图片、资源文件
│ └── Themes/ # 全局样式、字典
└── docs/ # 全套规范文档


## 三、开发规范
1. 全程遵循 C# 官方命名、缩进、注释规范
2. WPF 严格使用 MVVM 分层，后台代码禁止写业务
3. XAML 样式统一管理，避免内联重复样式
4. 禁止魔法数字、硬编码密钥、低效冗余代码

## 四、架构设计
分层结构：
View → ViewModel → Model → Service
- 界面只负责展示
- 逻辑全部放在 ViewModel
- 数据与业务解耦，通过 Service 统一调用

## 五、安全规范
- 全局异常捕获，日志留存
- 敏感数据加密、配置脱敏
- 限制多开、权限管控
- 正式发布移除调试信息
