# Taro 微信小程序项目 - 文档索引

欢迎来到青岛潮汐数据微信小程序项目！本文档将帮助你快速找到所需的信息。

## 📚 文档导航

### 新手入门
| 文档 | 描述 | 何时阅读 |
|------|------|--------|
| [QUICK_START.md](./QUICK_START.md) | 快速开始指南 | 第一次接触项目 |
| [README.md](./README.md) | 项目总体说明 | 了解项目功能 |
| [CONVERSION_SUMMARY.md](./CONVERSION_SUMMARY.md) | 转换总结 | 了解改进和变化 |

### 深入了解
| 文档 | 描述 | 何时阅读 |
|------|------|--------|
| [CONVERSION_GUIDE.md](./CONVERSION_GUIDE.md) | Web到小程序转换详解 | 理解架构变化 |
| [ARCHITECTURE.md](./ARCHITECTURE.md) | 系统架构文档 | 学习代码组织 |
| [PROJECT_CONFIG_GUIDE.md](./PROJECT_CONFIG_GUIDE.md) | 项目配置说明 | 配置AppID和白名单 |

### 发布前检查
| 文档 | 描述 | 何时阅读 |
|------|------|--------|
| [MIGRATION_CHECKLIST.md](./MIGRATION_CHECKLIST.md) | 迁移检查清单 | 发布前完成 |

## 🚀 快速开始 (5分钟)

```bash
# 1. 安装依赖
cd miniApp
npm install

# 2. 启动开发服务
npm run dev:weapp

# 3. 打开微信开发者工具
# 新建项目 → 选择 miniApp/dist/weapp
```

## 📁 项目结构速览

```
miniApp/
├── src/                      # 源代码
│   ├── pages/               # 页面
│   ├── components/          # 组件
│   ├── api/                # API层
│   ├── utils/              # 工具函数
│   ├── types/              # 类型定义
│   └── app.config.ts       # 应用配置
├── dist/                    # 编译输出
│   └── weapp/              # 小程序代码
├── 配置文件
│   ├── taro.config.ts      # Taro配置
│   ├── project.config.json # 小程序配置
│   └── tsconfig.json       # TypeScript配置
└── 文档
    ├── README.md           # 项目说明
    ├── QUICK_START.md      # 快速开始
    └── ...其他文档
```

## 🔧 常见任务

### 我想...

**启动开发服务**
```bash
npm run dev:weapp
```
👉 参考: [QUICK_START.md](./QUICK_START.md#开发模式)

**添加新页面**
- 在 `src/pages/` 创建新文件夹
- 添加到 `src/app.config.ts` 的 `pages` 数组
👉 参考: [ARCHITECTURE.md](./ARCHITECTURE.md#扩展点)

**修改导航栏样式**
👉 编辑 `src/app.config.ts` 中的 `window` 配置

**构建生产版本**
```bash
npm run build:weapp
```
👉 参考: [README.md](./README.md#构建)

**配置微信小程序AppID**
👉 编辑 `project.config.json` 中的 `appid` 字段

**配置网络白名单**
👉 参考: [PROJECT_CONFIG_GUIDE.md](./PROJECT_CONFIG_GUIDE.md#网络白名单配置)

**理解代码架构**
👉 参考: [ARCHITECTURE.md](./ARCHITECTURE.md)

**了解Web到小程序的改动**
👉 参考: [CONVERSION_GUIDE.md](./CONVERSION_GUIDE.md)

## 📊 技术栈

- **Taro 3** - 跨端开发框架
- **React 18** - UI框架
- **TypeScript** - 类型安全
- **Canvas API** - 图表绘制
- **Taro.request** - 网络请求
- **SCSS** - 样式预处理

## ✨ 核心特性

- ✅ 潮汐数据实时获取
- ✅ Canvas高性能图表
- ✅ 农历日期显示
- ✅ 汛型智能判断
- ✅ 完整的错误处理
- ✅ 响应式设计

## 📝 文档速查表

### 按功能模块

**页面开发**
- [QUICK_START.md](./QUICK_START.md) - 页面开发快速指南
- [ARCHITECTURE.md](./ARCHITECTURE.md#组件树) - 组件树结构

**API和数据**
- [ARCHITECTURE.md](./ARCHITECTURE.md#数据流) - 数据流详解
- [CONVERSION_GUIDE.md](./CONVERSION_GUIDE.md#数据获取) - API调用方式

**样式和UI**
- [CONVERSION_GUIDE.md](./CONVERSION_GUIDE.md#样式转换) - 样式系统说明
- [ARCHITECTURE.md](./ARCHITECTURE.md#样式系统) - 样式架构

**图表和绘制**
- [ARCHITECTURE.md](./ARCHITECTURE.md#tidechartrenderter-图表渲染器) - 图表渲染详解
- [CONVERSION_GUIDE.md](./CONVERSION_GUIDE.md#图表绘制) - Chart.js迁移

**配置和部署**
- [PROJECT_CONFIG_GUIDE.md](./PROJECT_CONFIG_GUIDE.md) - 项目配置详解
- [MIGRATION_CHECKLIST.md](./MIGRATION_CHECKLIST.md) - 发布检查清单

### 按场景

**完全新手**
1. 阅读 [README.md](./README.md)
2. 按照 [QUICK_START.md](./QUICK_START.md) 安装和运行
3. 查看页面源代码理解结构

**要修改功能**
1. 查看 [ARCHITECTURE.md](./ARCHITECTURE.md#分层设计) 理解层级
2. 找到对应的源文件
3. 根据现有代码模式进行修改

**要添加功能**
1. 参考 [ARCHITECTURE.md](./ARCHITECTURE.md#扩展点)
2. 选择合适的层级添加代码
3. 按照现有样式和规范编写

**要发布小程序**
1. 完成 [MIGRATION_CHECKLIST.md](./MIGRATION_CHECKLIST.md)
2. 按照 [PROJECT_CONFIG_GUIDE.md](./PROJECT_CONFIG_GUIDE.md) 配置
3. 运行 `npm run build:weapp`
4. 用微信开发者工具打开 `dist/weapp`

**要优化性能**
1. 查看 [ARCHITECTURE.md](./ARCHITECTURE.md#性能优化)
2. 参考 [CONVERSION_SUMMARY.md](./CONVERSION_SUMMARY.md#性能对比) 的优化建议

## 🎯 学习路径

```
入门 → 开发 → 优化 → 发布

   ↓
QUICK_START.md
   ↓
README.md
   ↓
根据需要选择文档...
   ↓
ARCHITECTURE.md / CONVERSION_GUIDE.md
   ↓
实际编码和测试
   ↓
MIGRATION_CHECKLIST.md
   ↓
发布到微信小程序
```

## 🐛 遇到问题？

### 问题排查步骤

1. **阅读相关文档** - 大多数问题在文档中都有说明
2. **检查QUICK_START** - 常见问题解答部分
3. **查看ARCHITECTURE** - 理解设计原理
4. **使用微信开发者工具调试** - 查看console和network
5. **Google搜索错误信息** - 如 "Taro xxx error"

### 常见问题

**"找不到文件"**
→ 检查文件路径，注意是否区分大小写

**"网络请求失败"**
→ 参考 [PROJECT_CONFIG_GUIDE.md](./PROJECT_CONFIG_GUIDE.md#网络白名单配置)

**"样式不生效"**
→ 参考 [CONVERSION_GUIDE.md](./CONVERSION_GUIDE.md#样式转换)

**"编译失败"**
→ 查看console报错信息，或参考 [QUICK_START.md](./QUICK_START.md#常见问题)

## 📞 更多资源

### 官方文档
- [Taro文档](https://taro-docs.jd.com/)
- [微信小程序文档](https://developers.weixin.qq.com/miniprogram/)
- [React文档](https://react.dev/)

### 相关教程
- [Taro入门教程](https://taro-docs.jd.com/docs/guide)
- [Canvas教程](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
- [TypeScript教程](https://www.typescriptlang.org/docs/)

### 社区资源
- [Taro社区](https://github.com/NervJS/taro)
- [微信小程序社区](https://github.com/topics/weixin-miniprogram)

## ✅ 快速检查清单

开始前：
- [ ] 已安装Node.js >= 12.0
- [ ] 已安装npm或yarn
- [ ] 已下载微信开发者工具

第一步：
- [ ] 已运行 `npm install`
- [ ] 已运行 `npm run dev:weapp`
- [ ] 已打开微信开发者工具

发布前：
- [ ] 已完成 MIGRATION_CHECKLIST.md
- [ ] 已配置AppID
- [ ] 已配置白名单
- [ ] 已测试功能

## 📈 项目信息

- **项目名**: qingdao-tide-miniapp
- **类型**: 微信小程序
- **框架**: Taro + React
- **版本**: 1.0.0
- **状态**: ✅ 生产就绪

---

**需要帮助？** 检查相关文档或阅读源代码注释。

**祝开发愉快！** 🚀
