## ADDED Requirements

### Requirement: Population Growth (人口增长)
如果满足条件，系统必须随时间增加人口。

#### Scenario: Growth Conditions (增长条件)
- **WHEN** 住房容量 > 当前人口
- **AND** 幸福度 > 50%
- **THEN** 人口每天增加 X

### Requirement: Basic Needs (基本需求)
系统必须根据人口数量扣除资源。

#### Scenario: Daily Consumption (每日消耗)
- **WHEN** 每日更新发生时
- **THEN** 从食物库存中扣除 (人口 * 人均食物消耗)
- **AND** 从水库存中扣除 (人口 * 人均水消耗)

### Requirement: Happiness Calculation (幸福度计算)
系统必须基于需求满足情况计算幸福度。

#### Scenario: Needs Met (需求满足)
- **WHEN** 食物和水供应充足
- **THEN** 幸福度趋向 100%

#### Scenario: Starvation (饥荒)
- **WHEN** 食物耗尽
- **THEN** 幸福度迅速下降
- **AND** 人口开始死亡/流失（如果幸福度 < 0%）