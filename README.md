# 🌍 GEO 智能内容中台 - 整合版

> **专为出海企业设计的智能内容生成平台**  
> 支持美国、加拿大、英国、德国、法国、澳大利亚、日本、新加坡等8个主要海外市场

## 🚀 **快速开始**

### **1. 安装依赖**
```bash
pip install -r requirements.txt
```

### **2. 配置API密钥**
编辑 `geo_content_platform.py` 文件中的 `Settings` 类：
```python
class Settings:
    def __init__(self):
        self.google_api_key = "your_google_gemini_api_key"      # 替换为您的Gemini API密钥
        self.anthropic_api_key = "your_anthropic_claude_api_key" # 替换为您的Claude API密钥
        self.mota_access_token = "ms-14bd4f7d-1b74-42e5-9ded-fcbbbbd79619"  # 已配置DeepSeek
```

### **3. 启动服务**
```bash
python geo_content_platform.py
```

### **4. 访问应用**
- **主页面**: http://localhost:8000
- **海外内容生成**: http://localhost:8000/overseas
- **API文档**: http://localhost:8000/docs

## 🌍 **核心功能**

### **海外内容生成**
- **8个主要海外市场**：美国、加拿大、英国、德国、法国、澳大利亚、日本、新加坡
- **文化本地化**：根据目标市场文化特点生成内容
- **多AI模型**：同时调用 Gemini、Claude、DeepSeek 三个模型
- **内容类型**：社交媒体、营销文案、博客文章、邮件营销

### **GEO优化功能**
- **平台优化**：针对不同平台（社交媒体、搜索引擎等）优化内容
- **目标优化**：根据目标（互动、转化、知名度、流量）优化策略
- **智能建议**：提供具体的优化建议和最佳实践

## 📡 **API接口**

### **生成海外内容**
```bash
POST /api/v1/overseas_content/generate
{
    "prompt": "推广我们的AI产品",
    "target_market": "USA",
    "content_type": "social_media",
    "tone": "professional"
}
```

### **获取支持的市场**
```bash
GET /api/v1/overseas_content/markets
```

### **GEO优化**
```bash
POST /api/v1/geo_optimize
{
    "prompt": "优化我们的营销内容",
    "platform": "social_media",
    "goal": "engagement"
}
```

## 🎯 **使用示例**

### **生成美国市场社交媒体内容**
1. 访问 http://localhost:8000/overseas
2. 输入提示："推广我们的AI产品"
3. 选择市场：🇺🇸 美国
4. 选择类型：社交媒体
5. 选择语调：专业
6. 点击"生成海外内容"

### **API调用示例**
```python
import requests

# 生成海外内容
response = requests.post("http://localhost:8000/api/v1/overseas_content/generate", json={
    "prompt": "推广我们的AI产品",
    "target_market": "USA",
    "content_type": "social_media",
    "tone": "professional"
})

print(response.json())
```

## 📊 **支持的市场**

| 市场 | 文化特点 | 内容偏好 |
|------|----------|----------|
| 🇺🇸 美国 | 个人主义、效率导向、创新精神 | 简洁明了、数据驱动、实用性强 |
| 🇨🇦 加拿大 | 多元文化、环保意识、包容性 | 包容性强、环保理念、文化多样性 |
| 🇬🇧 英国 | 传统创新、品质细节、绅士风度 | 品质感强、细节丰富、幽默元素 |
| 🇩🇪 德国 | 质量可靠、数据驱动、严谨认真 | 技术性强、数据详实、逻辑清晰 |
| 🇫🇷 法国 | 艺术文化、生活品质、浪漫情怀 | 艺术感强、生活化、情感丰富 |
| 🇦🇺 澳大利亚 | 轻松友好、户外活动、平等主义 | 轻松自然、户外相关、平等友好 |
| 🇯🇵 日本 | 细节品质、传统礼仪、团队合作 | 细节丰富、礼仪规范、团队价值 |
| 🇸🇬 新加坡 | 多元文化、教育创新、国际化 | 多元包容、教育价值、国际视野 |

## 🔧 **技术架构**

- **后端框架**: FastAPI
- **AI模型**: Google Gemini + Anthropic Claude + DeepSeek-V3.1
- **异步处理**: asyncio
- **数据验证**: Pydantic
- **HTTP客户端**: httpx

## 📝 **文件说明**

- `geo_content_platform.py` - 主程序文件（包含所有功能）
- `requirements.txt` - Python依赖包
- `README.md` - 使用说明

## 🚀 **部署说明**

### **本地运行**
```bash
python geo_content_platform.py
```

### **生产环境**
```bash
# 使用gunicorn
pip install gunicorn
gunicorn geo_content_platform:app -w 4 -k uvicorn.workers.UvicornWorker

# 或使用uvicorn
uvicorn geo_content_platform:app --host 0.0.0.0 --port 8000
```

## 📞 **支持**

如有问题，请查看：
- API文档：http://localhost:8000/docs
- 健康检查：http://localhost:8000/api/v1/health

---

**🌍 让我们一起构建更好的海外内容生成平台！**
