## ADDED Requirements

### Requirement: Resource Definitions (资源定义)
系统必须追踪以下基础资源：
- **Power (电力)**: 瞬时供需平衡。不进行存储（MVP阶段）。
- **Water (水)**: 可存储资源。
- **Food (食物)**: 可存储资源。
- **Materials (建材)**: 用于建造的可存储资源。

#### Scenario: Resource Initialization (资源初始化)
- **WHEN** 新游戏开始时
- **THEN** 系统初始化资源起始值（例如：建材 100，食物 50）

### Requirement: Global Resource Pool (全局资源池)
系统必须维护一个全局库存，用于存储水、食物和建材，所有实体均可访问。

#### Scenario: Consuming materials (消耗建材)
- **WHEN** 建造一个消耗 50 建材的建筑
- **THEN** 立即从全局池中扣除 50 建材

### Requirement: Power Grid Logic (电网逻辑)
系统必须将电力计算为（总供给 - 总需求）的平衡值。电力不累积。

#### Scenario: Power Surplus (电力盈余)
- **WHEN** 供给 > 需求
- **THEN** 电网状态为“稳定 (Stable)”

#### Scenario: Power Deficit (电力赤字)
- **WHEN** 供给 < 需求
- **THEN** 电网状态为“过载 (Overloaded)”，部分建筑可能会停工

### Requirement: Production and Consumption Cycles (产消循环)
系统必须以固定间隔（游戏 Tick）更新资源总量。

#### Scenario: Tick Update (Tick 更新)
- **WHEN** 发生一次游戏 Tick（例如每 1 秒）
- **THEN** 计算每种资源的（总产出 - 总消耗），并将净变化应用到全局池