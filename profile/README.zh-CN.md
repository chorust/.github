# Chorust

**为数据、智能体与智能系统构建可组合的基础能力。**

Chorust 是一个开源组织，专注于构建系统、数据与 AI 基础设施工具，并以 Rust 作为核心技术之一。

每个项目都应该能够独立存在：足够聚焦，边界清晰，同时又能够与生态中的其他工具组合使用。

**独立成声，协作成章。**

[English](README.md)

## 项目

### [Chorust](https://github.com/chorust/chorust)

**本地优先的 Coding Agent 会话观测与控制。**

Chorust 通过 Coding Agent 原生且公开的接口观察其运行状态，同时保持 Agent 自身的日志、Prompt、存储和执行路径只读。

它将 Agent 活动转化为可观察的状态和受控操作，并为推断保留明确的证据、能力边界和保守的安全默认值。

### [Radiust](https://github.com/chorust/radiust)

**雷达数据获取与处理基础设施。**

Radiust 为来自不同提供方的天气雷达数据提供统一的发现、获取、解码、验证、缓存和导出工具链。

Python 提供面向用户的数据与 CLI 层，Rust 则负责受限 I/O、缓存、临时存储以及底层基础设施能力。

### [DuckJeu](https://github.com/chorust/duckjeu)

**让 Judgment 成为 SQL Primitive。**

DuckJeu 是一个 DuckDB 扩展，将 JEV 风格的概率判断和分类判断直接带入 SQL。

```sql
SELECT jev_bool(
    message,
    'the customer requests a refund'
)
FROM tickets;
```

Judgment 因而成为具有明确类型的数据，可以像普通关系数据一样参与过滤、聚合、Join、缓存和组合。

### [DuckOMo](https://github.com/chorust/duckomo)

**直接使用 DuckDB 查询 Open-Meteo OM 数据。**

DuckOMo 是规划中的 DuckDB 扩展，将 SQL 的列投影以及时空条件转换为 OM 逻辑数组切片。

目标很简单：只读取查询真正需要的数据，而不必首先完整加载或转换整个 OM 文件。

### [Conductorust](https://github.com/chorust/conductorust)

**Spec Compiler。**

一个处于早期阶段的项目，探索如何把结构化 Specification 转换为可执行或机器可消费的表示。

## 设计原则

我们偏爱这样的软件：

- **聚焦（Focused）** —— 先把一个职责做好，再考虑成为大平台
- **可组合（Composable）** —— 可以独立使用，也可以组合产生更大的能力
- **明确（Explicit）** —— 清晰的契约、边界与失败模式
- **尽可能本地优先（Local-first）** —— 尽量让控制权和数据留在用户身边
- **证据驱动（Evidence-driven）** —— 明确区分已经实现、已经验证、推断得到和仍在规划中的能力
- **Rust at the core** —— 尤其是在正确性、性能和系统集成重要的地方

## 为什么叫 Chorust？

合唱由彼此独立的声音组成。

每一个声部都有自己的角色、音域与身份。最终的整体并非来自所有声音变得相同，而是来自它们之间的协作。

我们希望软件也是如此。

**它们不需要成为一个庞大的统一平台，只需要彼此独立，又能协同工作。**
