## ADDED Requirements

### Requirement: Disaster Types (灾害类型)
系统必须支持多种具有不同效果的灾害定义。

#### Scenario: Heatwave Effect (热浪效果)
- **WHEN** 热浪活跃时
- **THEN** 人口的水消耗增加 50%
- **AND** 农场产出减少 20%

#### Scenario: Power Failure Effect (电力故障效果)
- **WHEN** 电力故障事件触发
- **THEN** 随机一个发电厂变为 "Damaged" 状态或产出降为 0

### Requirement: Disaster Lifecycle (灾害生命周期)
灾害必须遵循阶段性推进：Warning (预警) -> Active (活跃) -> Resolved (结束)。

#### Scenario: Warning Phase (预警阶段)
- **WHEN** 灾害计划在 X Ticks 后开始
- **THEN** UI 显示倒计时警告

### Requirement: Global Modifier System (全局修正系统)
系统必须支持灾害可应用的全局修正器。

#### Scenario: Applying Modifiers (应用修正)
- **WHEN** 灾害开始
- **THEN** 向全局状态注册一个临时修正器（例如 "WaterConsumptionMult: 1.5"）