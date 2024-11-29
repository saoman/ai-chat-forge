# Document.AI

基于向量数据库与GPT3.5的通用本地知识库方案(A universal local knowledge base solution based on vector database and GPT3.5)

## 项目简介

这是一个基于向量数据库(Qdrant)与GPT3.5的通用本地知识库解决方案。主要功能是将本地文档数据转换为向量存储,然后通过语义搜索与GPT结合来实现智能问答。

## 目录结构

```bash
.
├── code/               # 示例代码
│   ├── server/        # 服务端代码
│   ├── data_import/   # 数据导入代码
│   └── test/          # 测试代码
└── docs/              # 文档和设计思考
```

## 核心功能

1. **文档向量化**: 
   - 支持多种格式文档导入(txt, excel等)
   - 使用OpenAI Embedding API进行向量转换
   - 存储到Qdrant向量数据库

2. **智能问答**:
   - 问题向量化搜索
   - 相似度匹配
   - 使用GPT优化回答内容

## 工作流程
1. 数据预处理:
   - 将本地文档数据转换为向量
   - 存储到Qdrant向量数据库中
2. 查询过程:
   - 用户输入问题
   - 将问题转换为向量
   - 从向量数据库中检索相似内容
   - 使用GPT优化回答内容


### 2. 安装依赖

1. 服务端:
   ```bash
   cd code/server
   pip install -r requirements.txt
   ```

2. 数据导入:
   ```bash
   cd code/data_import
   pip install -r requirements.txt
   ```

3. 配置
   设置OpenAI API密钥:
   ```bash
   export OPENAI_API_KEY=sk-xxxxxx
   ```

4. 运行
   启动服务:
     ```bash
     cd code/server
     python server.py
     ```
    访问地址: http://localhost:3000
