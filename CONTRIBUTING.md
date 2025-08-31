# 🤝 贡献指南

感谢您对 GEO 智能内容中台项目的关注！我们欢迎所有形式的贡献。

## 📋 贡献类型

### 🐛 Bug 报告
如果您发现了 bug，请通过以下方式报告：
1. 使用 GitHub Issues 创建新的 issue
2. 提供详细的复现步骤
3. 包含错误日志和截图
4. 标注问题类型和优先级

### 💡 功能建议
如果您有新功能的想法，请：
1. 先检查是否已有相关 issue
2. 创建新的 feature request issue
3. 详细描述功能需求和用例
4. 讨论实现方案

### 🔧 代码贡献
如果您想贡献代码：
1. Fork 项目仓库
2. 创建功能分支
3. 编写代码和测试
4. 提交 Pull Request

## 🛠️ 开发环境设置

### 1. 克隆项目
```bash
git clone https://github.com/yourusername/geo-content-platform.git
cd geo-content-platform
```

### 2. 创建虚拟环境
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# 或
venv\Scripts\activate  # Windows
```

### 3. 安装依赖
```bash
pip install -r requirements.txt
```

### 4. 配置环境变量
```bash
cp env.example .env
# 编辑 .env 文件，配置必要的 API 密钥
```

### 5. 运行测试
```bash
python -m pytest
```

## 📝 代码规范

### Python 代码规范
- 遵循 PEP 8 代码风格
- 使用类型注解
- 添加详细的文档字符串
- 使用有意义的变量名

### 提交信息规范
使用清晰的提交信息：
```
feat: 添加新功能
fix: 修复 bug
docs: 更新文档
style: 代码格式调整
refactor: 代码重构
test: 添加测试
chore: 构建过程或辅助工具的变动
```

### 分支命名规范
- `feature/功能名称` - 新功能
- `fix/问题描述` - Bug 修复
- `docs/文档更新` - 文档更新
- `refactor/重构描述` - 代码重构

## 🔍 代码审查

### Pull Request 要求
1. **功能完整**: 确保功能按预期工作
2. **测试覆盖**: 添加必要的单元测试
3. **文档更新**: 更新相关文档
4. **代码质量**: 通过代码审查
5. **CI 通过**: 所有 CI 检查通过

### 审查清单
- [ ] 代码符合项目规范
- [ ] 添加了必要的测试
- [ ] 更新了相关文档
- [ ] 提交信息清晰明确
- [ ] 没有引入新的警告或错误

## 🧪 测试指南

### 运行测试
```bash
# 运行所有测试
python -m pytest

# 运行特定测试文件
python -m pytest tests/test_overseas_content.py

# 运行带覆盖率的测试
python -m pytest --cov=app

# 运行性能测试
python -m pytest tests/test_performance.py
```

### 编写测试
- 为每个新功能编写测试
- 测试覆盖正常和异常情况
- 使用描述性的测试名称
- 遵循 AAA 模式 (Arrange, Act, Assert)

## 📚 文档贡献

### 文档类型
- **README.md**: 项目介绍和使用指南
- **API 文档**: 接口说明和示例
- **开发文档**: 开发环境设置和指南
- **用户手册**: 详细的使用说明

### 文档规范
- 使用清晰的标题结构
- 提供代码示例
- 包含截图和图表
- 保持文档的时效性

## 🚀 发布流程

### 版本号规范
使用语义化版本号 (SemVer):
- `MAJOR.MINOR.PATCH`
- 例如: `1.0.0`, `1.1.0`, `1.1.1`

### 发布步骤
1. 更新版本号
2. 更新 CHANGELOG.md
3. 创建 release tag
4. 发布到 PyPI (如果适用)

## 📞 联系我们

如果您有任何问题或建议：
- **GitHub Issues**: 创建 issue
- **邮箱**: your.email@example.com
- **讨论区**: GitHub Discussions

## 🙏 致谢

感谢所有为项目做出贡献的开发者！

---

**让我们一起构建更好的海外内容生成平台！** 🌍
