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
欧耶
