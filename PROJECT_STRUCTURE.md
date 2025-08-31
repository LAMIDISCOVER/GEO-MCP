# 📁 项目结构说明

## 🏗️ **整体架构**

```
geo-content-platform/
├── 📁 app/                    # 主应用目录
│   ├── 📄 main.py            # FastAPI主应用入口
│   ├── 📄 config.py          # 配置管理
│   ├── 📄 models.py          # 数据模型定义
│   ├── 📁 api/               # API路由层
│   ├── 📁 services/          # 服务层
│   ├── 📁 static/            # 前端静态文件
│   ├── 📁 tools/             # 工具系统
│   └── 📁 mcp/               # MCP协议实现
├── 📁 tests/                 # 测试文件
├── 📄 requirements.txt       # Python依赖
├── 📄 pyproject.toml        # 项目配置
├── 📄 env.example           # 环境变量示例
└── 📄 README.md             # 项目说明
```

## 📋 **核心模块说明**

### **🌐 API路由层 (`app/api/`)**
- `mcp.py` - MCP协议API路由
- `geo_content.py` - GEO内容生成API
- `geo_optimize.py` - DeepSeek优化API
- `geo_optimization.py` - GEO优化API
- `overseas_content.py` - **海外内容生成API** ⭐

### **🔧 服务层 (`app/services/`)**
- `ai_models.py` - AI模型服务（Gemini + Claude）
- `overseas_content.py` - **海外内容生成服务** ⭐
- `mota_service.py` - DeepSeek服务集成
- `geo_optimizer.py` - GEO优化器
- `health_checker.py` - 健康检查服务

### **💻 前端界面 (`app/static/`)**
- `index.html` - 主聊天界面
- `overseas.html` - **海外运营专用界面** ⭐
- `demo.html` - 功能演示界面
- `styles.css` - 样式文件
- `app.js` - 前端逻辑
- `manifest.json` - PWA配置
- `sw.js` - Service Worker

### **🛠️ 工具系统 (`app/tools/`)**
- `base.py` - 工具基类
- `registry.py` - 工具注册表
- `example_tools.py` - 示例工具

### **📡 MCP协议 (`app/mcp/`)**
- `protocol.py` - JSON-RPC 2.0协议实现
- `server.py` - MCP服务器
- `methods.py` - MCP方法实现

## 🎯 **核心功能模块**

### **海外内容生成模块** ⭐⭐⭐
```
app/services/overseas_content.py
├── OverseasContentGenerator类
├── 8个海外市场配置
│   ├── USA (美国)
│   ├── Canada (加拿大)
│   ├── UK (英国)
│   ├── Germany (德国)
│   ├── France (法国)
│   ├── Australia (澳大利亚)
│   ├── Japan (日本)
│   └── Singapore (新加坡)
├── 文化特点和内容偏好
├── 市场特定内容模板
└── 优化建议系统

app/api/overseas_content.py
├── 海外内容生成API
├── 多市场内容生成
├── 市场信息查询
└── 健康检查接口

app/static/overseas.html
├── 海外市场展示
├── 内容生成表单
├── 结果展示界面
└── 优化建议显示
```

### **AI模型集成模块**
```
app/services/ai_models.py
├── GEOContentGenerator类
├── GeminiService类
├── ClaudeService类
└── 异步并行处理

app/services/mota_service.py
├── MotaService类
├── DeepSeek API集成
├── Bearer Token认证
└── 错误处理机制
```

### **GEO优化功能模块**
```
app/services/geo_optimizer.py
├── GEOOptimizer类
├── 平台优化策略
├── 目标优化算法
└── 指标计算系统

app/api/geo_optimization.py
├── GEO优化API
├── 平台和目标查询
├── 优化策略接口
└── 健康检查
```

## 🔄 **数据流**

### **海外内容生成流程**
```
用户输入 → 前端界面 → API路由 → 服务层 → AI模型 → 结果聚合 → 响应
    ↓
文化适配 ← 市场配置 ← 内容模板 ← 优化建议 ← 本地存储
```

### **AI模型调用流程**
```
请求 → API路由 → 服务层 → 异步并行调用 → 结果聚合 → 响应
    ↓
Gemini API    Claude API    DeepSeek API
```

## 📊 **文件重要性评级**

### **⭐⭐⭐ 核心文件**
- `app/services/overseas_content.py` - 海外内容生成核心
- `app/api/overseas_content.py` - 海外内容API
- `app/static/overseas.html` - 海外运营界面
- `app/main.py` - 应用入口

### **⭐⭐ 重要文件**
- `app/services/ai_models.py` - AI模型服务
- `app/config.py` - 配置管理
- `app/services/mota_service.py` - DeepSeek服务
- `requirements.txt` - 依赖管理

### **⭐ 支持文件**
- `app/tools/` - 工具系统
- `app/mcp/` - MCP协议
- `app/static/` - 其他前端文件
- `tests/` - 测试文件

## 🚀 **扩展指南**

### **添加新市场**
1. 修改 `app/services/overseas_content.py`
2. 添加市场配置和文化特点
3. 更新 `app/static/overseas.html` 界面选项
4. 测试新市场功能

### **集成新AI模型**
1. 在 `app/services/` 中创建新服务类
2. 实现标准接口方法
3. 在 `app/api/` 中注册新端点
4. 更新前端调用逻辑

### **添加新内容类型**
1. 在 `app/services/overseas_content.py` 中添加内容类型
2. 创建对应的内容模板
3. 更新API和前端界面
4. 添加相应的测试

## 🔧 **开发环境**

### **目录结构**
- `app/` - 主应用代码
- `tests/` - 测试文件
- `docs/` - 文档文件（可选）
- `scripts/` - 脚本文件（可选）

### **配置文件**
- `requirements.txt` - Python依赖
- `pyproject.toml` - 项目配置
- `env.example` - 环境变量示例
- `.gitignore` - Git忽略文件

### **文档文件**
- `README.md` - 项目说明
- `CONTRIBUTING.md` - 贡献指南
- `CHANGELOG.md` - 更新日志
- `LICENSE` - 许可证

---

**💡 提示**: 标有 ⭐ 的文件是项目的核心文件，需要重点关注和维护。
