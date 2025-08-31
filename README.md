# Quant Backtest Platform  
一个从零实现的 **股票回测平台**，支持多策略回测、风险指标计算、结果可视化，并提供轻量级 Web 界面。  
本项目旨在帮助初学者理解 **量化研究平台的底层逻辑**，同时展现工程化能力。  

---

## 🚀 功能特点
- 📈 **多策略支持**：均线交叉、动量策略、随机策略（可扩展）  
- 💾 **数据模块**：支持 API (Tushare/Yahoo)、CSV、SQLite  
- ⚡ **回测引擎**：支持单股票/多股票组合，含交易费用 & 滑点模拟  
- 📊 **风险指标**：夏普比率、最大回撤、累计收益  
- 🎨 **可视化**：收益曲线、回撤曲线、买卖点标记  
- 🌐 **Web 界面（扩展）**：Flask/FastAPI 提供交互式回测入口  

---

## 🏗️ 项目架构

```mermaid
flowchart TD
    A[数据源 CSV/API] --> B[DataLoader]
    B --> C[策略 Strategy]
    C --> D[回测引擎 Backtester]
    D --> E[风险指标 Metrics]
    D --> F[可视化 Visualization]
    E --> G[报告/结果输出]
    F --> G
    D --> H[Web 界面 Flask/FastAPI]
````

---

## 📂 文件结构

```
quant-backtest-platform/
│── backtest/                # 核心模块
│   ├── data_loader.py       # 数据获取 & 清洗
│   ├── strategy.py          # 策略基类 & 策略实现
│   ├── backtester.py        # 回测引擎
│   ├── metrics.py           # 风险指标
│   ├── visualization.py     # 可视化
│   └── utils.py             # 工具函数
│── webapp/                  # Web 界面
│   ├── app.py               # Flask/FastAPI 服务
│   ├── templates/           # HTML 模板
│   └── static/              # 静态文件
│── examples/                # 示例代码
│   └── run_macross.py
│── tests/                   # 单元测试
│── data/                    # 数据存储
│── README.md
│── requirements.txt
```

---

## 🔧 技术栈

* **语言**：Python 3.9+
* **数据处理**：Pandas, NumPy
* **可视化**：Matplotlib, Plotly
* **Web 框架**：Flask / FastAPI
* **数据库**：SQLite / CSV
* **其他**：pytest（测试）、timeit（性能测试）

---

## 📥 安装与运行

1. **克隆项目**

```bash
git clone https://github.com/yourusername/quant-backtest-platform.git
cd quant-backtest-platform
```

2. **安装依赖**

```bash
pip install -r requirements.txt
```

3. **运行示例**

```bash
python examples/run_macross.py
```

4. **启动 Web 界面（可选）**

```bash
cd webapp
python app.py
```

访问 `http://127.0.0.1:5000/`

---


### ✅ 收益曲线

### ✅ 策略对比


## 🧪 测试



## 📌 未来计划 (Roadmap)

* [ ] 增加更多策略（RSI, MACD, Pair Trading）
* [ ] 支持分钟级数据回测
* [ ] 并行计算（多核加速）
* [ ] Docker 部署
* [ ] Web 前端可视化增强（React + Plotly）

---

## ✨ 项目亮点

* 独立设计并实现了股票回测平台，支持 **多策略组合、百万级数据秒级处理**
* 实现夏普比率、最大回撤等金融风险指标
* 封装 CLI & Web 界面，提升用户体验
* GitHub 开源项目，具备清晰架构 & 工程化能力

---

## 👨‍💻 作者

* **zhaojj** （软件工程本科 / 量化 & AI 系统学习者）
* 📫 联系方式: zhaojjl0l0@gmail

```

---


