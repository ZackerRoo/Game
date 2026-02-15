## ADDED Requirements

### Requirement: Building Entities (建筑实体)
系统必须支持具有特定产出/消耗率的不同建筑类型。

#### Scenario: Building a Farm (建造农场)
- **WHEN** 玩家建造一个农场
- **THEN** 需要消耗建材进行建造
- **AND** 一旦激活，它每 Tick 消耗水并产出食物

### Requirement: Grid Placement (网格放置)
系统必须限制建筑只能放置在网格上。

#### Scenario: Valid Placement (有效放置)
- **WHEN** 玩家尝试将建筑放置在地图边界内的空地块上
- **THEN** 允许放置

#### Scenario: Invalid Placement (无效放置/碰撞)
- **WHEN** 玩家尝试将建筑放置在已被占用的地块上
- **THEN** 拒绝放置

### Requirement: Operational States (运行状态)
建筑必须具有以下状态：Active (活跃), Disabled (玩家关闭), NoPower (无电自动关闭), Damaged (受损)。

#### Scenario: Power Cut (断电)
- **WHEN** 电网过载
- **THEN** 非必要建筑（如工厂）切换到 "NoPower" 状态并停止生产

### Requirement: Maintenance (维护)
建筑需要维护成本（MVP 第一阶段可选，但为第二阶段预留规格）。

#### Scenario: Degradation (老化/受损 - 未来规划)
- **WHEN** 灾害发生
- **THEN** 建筑健康度下降