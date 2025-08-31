# 🌍 GEO 智能内容中台 - 海外运营专用平台

> **专为出海企业设计的智能内容生成平台**  
> 支持美国、加拿大、英国、德国、法国、澳大利亚、日本、新加坡等8个主要海外市场

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green.svg)](https://fastapi.tiangolo.com)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 🚀 **核心功能**

### 🌍 **海外市场内容生成**
- **8个主要海外市场**：美国、加拿大、英国、德国、法国、澳大利亚、日本、新加坡
- **文化本地化**：根据目标市场文化特点生成内容
- **语言适配**：自动使用当地语言习惯和表达方式
- **时区优化**：考虑当地时区安排发布时间
- **货币本地化**：使用当地货币符号和价格格式

### 🤖 **多AI模型并行处理**
- **双AI模型**：同时调用 Google Gemini 和 Anthropic Claude
- **DeepSeek集成**：通过ModelScope集成DeepSeek-V3.1
- **异步处理**：并行生成，提高响应速度
- **结果聚合**：智能整合多个模型的输出

### 🎯 **内容类型支持**
- **📱 社交媒体**：Facebook、Twitter、LinkedIn、Instagram
- **📢 营销文案**：广告文案、产品介绍、品牌宣传
- **📝 博客文章**：技术博客、行业分析、产品教程
- **📧 邮件营销**：Newsletter、促销邮件、客户沟通

### 🔧 **智能优化功能**
- **DeepSeek优化**：集成DeepSeek-V3.1模型进行内容优化
- **GEO优化**：生成引擎优化，提高AI模型推送效果
- **文化适配**：自动调整内容风格适应目标市场
- **SEO优化**：针对搜索引擎优化的内容生成

### 💬 **现代化聊天界面**
- **实时对话**：支持与AI进行自然语言对话
- **离线支持**：无网络时仍可使用基础功能
- **本地存储**：聊天记录保存在本地，保护隐私
- **PWA支持**：可安装为桌面应用

## 🎯 **应用场景**

### 🏢 **企业出海**
- **市场进入**：为新产品进入海外市场生成本地化内容
- **品牌推广**：创建符合当地文化的品牌宣传材料
- **客户沟通**：生成适合当地客户的沟通内容
- **营销活动**：为海外营销活动创建定制化内容

### 📱 **社交媒体运营**
- **多平台内容**：为不同社交媒体平台生成适配内容
- **话题营销**：基于热门话题生成相关内容
- **用户互动**：创建促进用户互动的内容
- **品牌建设**：建立符合当地文化的品牌形象

### 📧 **邮件营销**
- **Newsletter**：创建专业的邮件通讯内容
- **促销邮件**：生成有效的促销和推广邮件
- **客户关怀**：制作客户关怀和跟进邮件
- **活动邀请**：设计活动邀请和通知邮件

### 📝 **内容创作**
- **技术博客**：生成技术分享和教程文章
- **行业分析**：创建行业趋势和分析报告
- **产品介绍**：制作产品功能和使用指南
- **案例分享**：编写客户成功案例和故事

## 🛠️ **技术架构**

### **后端技术栈**
- **FastAPI**：高性能异步Web框架
- **Pydantic**：数据验证和序列化
- **Uvicorn**：ASGI服务器
- **Python 3.9+**：现代Python特性支持

### **AI模型集成**
- **Google Gemini**：Google最新AI模型
- **Anthropic Claude**：Anthropic的Claude模型
- **DeepSeek-V3.1**：通过ModelScope集成的DeepSeek模型
- **异步调用**：并发处理多个AI模型请求

### **前端技术**
- **原生JavaScript**：轻量级前端实现
- **CSS3**：现代化样式设计
- **PWA**：渐进式Web应用
- **Service Worker**：离线功能支持

## 📦 **快速开始**

### **1. 环境要求**
```bash
Python 3.9+
pip 20.0+
```

### **2. 克隆项目**
```bash
git clone https://github.com/yourusername/geo-content-platform.git
cd geo-content-platform
```

### **3. 安装依赖**
```bash
pip install -r requirements.txt
```

### **4. 配置环境变量**
```bash
cp env.example .env
```

编辑 `.env` 文件，配置您的API密钥：
```env
# AI模型API密钥
GOOGLE_API_KEY=your_google_gemini_api_key
ANTHROPIC_API_KEY=your_anthropic_claude_api_key

# DeepSeek API配置
MOTA_ACCESS_TOKEN=your_deepseek_api_key
MOTA_API_BASE_URL=https://api-inference.modelscope.cn/v1

# 服务器配置
HOST=0.0.0.0
PORT=8000
DEBUG=True
```

### **5. 启动服务**
```bash
python -m app.main
```

### **6. 访问应用**
- **主界面**: http://localhost:8000/
- **海外运营平台**: http://localhost:8000/overseas
- **功能演示**: http://localhost:8000/demo
- **API文档**: http://localhost:8000/docs

## 🌐 **使用指南**

### **海外内容生成**

#### **1. 选择目标市场**
- 美国 (USA) - 个人主义、效率导向
- 加拿大 (Canada) - 多元文化、环保意识
- 英国 (UK) - 传统创新、品质细节
- 德国 (Germany) - 质量可靠、数据驱动
- 法国 (France) - 艺术文化、生活品质
- 澳大利亚 (Australia) - 轻松友好、户外活动
- 日本 (Japan) - 细节品质、传统礼仪
- 新加坡 (Singapore) - 多元文化、教育创新

#### **2. 选择内容类型**
- **社交媒体**: 适合Facebook、Twitter等平台
- **营销文案**: 用于广告和产品推广
- **博客文章**: 技术分享和行业分析
- **邮件营销**: Newsletter和客户沟通

#### **3. 设置参数**
- **语调风格**: 专业、轻松、友好、正式
- **内容长度**: 简短、中等、详细
- **内容提示**: 描述您要生成的内容

#### **4. 生成内容**
点击"生成海外内容"按钮，系统将：
- 分析目标市场文化特点
- 构建市场特定的提示词
- 调用AI模型生成内容
- 提供优化建议

### **API使用示例**

#### **生成海外内容**
```bash
curl -X POST "http://localhost:8000/api/v1/overseas_content/generate" \
  -H "Content-Type: application/json" \
  -d '{
    "prompt": "推广我们的AI产品",
    "target_market": "USA",
    "content_type": "social_media",
    "tone": "professional"
  }'
```

#### **获取支持的市场**
```bash
curl "http://localhost:8000/api/v1/overseas_content/markets"
```

#### **健康检查**
```bash
curl "http://localhost:8000/api/v1/overseas_content/health"
```

## 📊 **功能特性对比**

| 功能 | 基础版 | 海外版 | 企业版 |
|------|--------|--------|--------|
| 支持市场 | 全球通用 | 8个海外市场 | 全球+定制 |
| AI模型 | Gemini + Claude | Gemini + Claude + DeepSeek | 全模型支持 |
| 内容类型 | 4种 | 4种 | 8种+ |
| 文化适配 | 基础 | 深度本地化 | 完全定制 |
| 优化功能 | 基础 | GEO优化 | 高级优化 |
| 离线支持 | ✅ | ✅ | ✅ |
| 本地存储 | ✅ | ✅ | ✅ |

## 🔧 **开发指南**

### **项目结构**
```
geo-content-platform/
├── app/
│   ├── main.py                 # FastAPI主应用
│   ├── config.py               # 配置管理
│   ├── models.py               # 数据模型
│   ├── api/                    # API路由
│   │   ├── mcp.py             # MCP协议API
│   │   ├── geo_content.py     # GEO内容生成API
│   │   ├── geo_optimize.py    # DeepSeek优化API
│   │   ├── geo_optimization.py # GEO优化API
│   │   └── overseas_content.py # 海外内容API
│   ├── services/               # 服务层
│   │   ├── ai_models.py       # AI模型服务
│   │   ├── overseas_content.py # 海外内容服务
│   │   ├── mota_service.py    # DeepSeek服务
│   │   └── geo_optimizer.py   # GEO优化器
│   ├── static/                 # 静态文件
│   │   ├── index.html         # 主界面
│   │   ├── overseas.html      # 海外运营界面
│   │   ├── demo.html          # 演示界面
│   │   ├── styles.css         # 样式文件
│   │   └── app.js             # 前端逻辑
│   └── tools/                  # 工具系统
│       ├── registry.py        # 工具注册表
│       └── example_tools.py   # 示例工具
├── requirements.txt            # Python依赖
├── env.example                 # 环境变量示例
└── README.md                   # 项目说明
```

### **添加新市场**
1. 在 `app/services/overseas_content.py` 中添加市场配置
2. 定义文化特点和内容偏好
3. 创建市场特定的内容模板
4. 更新前端界面选项

### **集成新AI模型**
1. 在 `app/services/` 中创建新的服务类
2. 实现标准的接口方法
3. 在API路由中注册新端点
4. 更新前端调用逻辑

## 🤝 **贡献指南**

欢迎提交 Issue 和 Pull Request！

- **Bug报告**: 使用GitHub Issues
- **功能建议**: 创建Feature Request
- **代码贡献**: Fork项目并提交PR
- **文档改进**: 帮助完善文档

详细贡献指南请查看 [CONTRIBUTING.md](CONTRIBUTING.md)

## 📄 **许可证**

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 📞 **联系我们**

- **项目主页**: https://github.com/yourusername/geo-content-platform
- **问题反馈**: https://github.com/yourusername/geo-content-platform/issues
- **邮箱**: your.email@example.com

## 🙏 **致谢**

感谢以下开源项目和服务：
- [FastAPI](https://fastapi.tiangolo.com/) - 现代、快速的Web框架
- [Google Gemini](https://ai.google.dev/) - Google AI模型
- [Anthropic Claude](https://www.anthropic.com/) - Claude AI模型
- [DeepSeek](https://www.deepseek.com/) - DeepSeek AI模型

---

**⭐ 如果这个项目对您有帮助，请给我们一个星标！**

**🌍 让我们一起构建更好的海外内容生成平台！**
