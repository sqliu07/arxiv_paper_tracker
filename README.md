# ArXiv论文追踪与分析器

一个自动追踪和分析arXiv最新论文的工具。该工具可以自动下载最近5天内发布的论文，并使用DeepSeek AI进行分析和总结。

## 功能特点

- 自动追踪最近5天内发布的AI、机器学习和NLP类别的论文
- 自动下载论文PDF
- 使用DeepSeek AI进行论文分析和总结
- 生成结构化的分析报告
- 自动清理下载的PDF文件以节省空间

## 安装

1. 克隆仓库：
```bash
git clone https://github.com/你的用户名/arxiv_paper_tracker.git
cd arxiv_paper_tracker
```

2. 安装依赖：
```bash
pip install -r requirements.txt
```

## 配置

1. 在`src/main.py`中设置你的DeepSeek API密钥：
```python
DEEPSEEK_API_KEY = "你的API密钥"
```

2. 可以修改以下参数来自定义追踪：
- `CATEGORIES`: 要追踪的arXiv类别（默认为["cs.AI", "cs.LG", "cs.CL"]）
- `MAX_PAPERS`: 每次运行处理的论文数量（默认为5）

## 使用方法

运行脚本：
```bash
cd src
python main.py
```

脚本会：
1. 搜索最近5天内发布的论文
2. 下载PDF文件
3. 使用DeepSeek AI分析论文
4. 生成分析报告
5. 自动删除PDF文件

分析结果将保存在`conclusion.md`文件中。

## 输出格式

分析报告包含以下内容：
- 论文标题
- 作者信息
- 论文类别
- 发布日期
- 论文链接
- AI分析结果，包括：
  - 简明摘要
  - 主要贡献和创新点
  - 研究方法和技术细节
  - 实验结果
  - 潜在影响
  - 局限性和未来工作

## 注意事项

- 请确保有足够的磁盘空间用于临时存储PDF文件
- 需要有效的DeepSeek API密钥
- 建议不要过于频繁地运行脚本，以避免API限制

## 许可证

MIT License 