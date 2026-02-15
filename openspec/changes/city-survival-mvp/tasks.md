## 1. Project Setup (项目设置)

- [ ] 1.1 初始化基于 React 和 TypeScript 的 Vite 项目。
- [ ] 1.2 设置项目目录结构 (src/game, src/components, src/assets)。
- [ ] 1.3 创建基础布局，包含 Canvas 容器和 UI 覆盖层。

## 2. Core Engine (核心引擎)

- [ ] 2.1 实现 `GameLoop` 类（启动、停止、Tick 循环）。
- [ ] 2.2 实现单例 `GameState` 以存储资源、地图和实体。
- [ ] 2.3 实现游戏对象的基础 Entity/Component 接口（或类型定义）。

## 3. Map System (地图系统)

- [ ] 3.1 实现 `MapSystem` 以生成和存储网格数据（地块类型：空、草地、水）。
- [ ] 3.2 实现网格的 Canvas 渲染（等轴或顶视）。
- [ ] 3.3 添加鼠标交互（悬停高亮、点击选择地块）。

## 4. Resource System (资源系统)

- [ ] 4.1 在 `GameState` 中定义资源类型和初始状态。
- [ ] 4.2 创建 `ResourceBar` UI 组件以显示当前资源。
- [ ] 4.3 实现 `ResourceSystem` 以处理资源的添加/移除操作。

## 5. Building System (建筑系统)

- [ ] 5.1 定义建筑数据结构（成本、尺寸、类型）。
- [ ] 5.2 实现 `BuildMenu` UI 以选择建筑。
- [ ] 5.3 实现放置逻辑（网格吸附、碰撞检测、成本检测）。
- [ ] 5.4 在地图上渲染已放置的建筑。

## 6. Simulation Logic (模拟逻辑)

- [ ] 6.1 实现 `ProductionSystem` 处理每 Tick 的建筑产出。
- [ ] 6.2 实现 `ConsumptionSystem` 处理人口需求和建筑维护。
- [ ] 6.3 将模拟更新连接到 `GameState` 和 UI。

## 7. Disaster System (灾害系统)

- [ ] 7.1 定义基础灾害类型（热浪）。
- [ ] 7.2 实现 `DisasterManager` 以触发事件。
- [ ] 7.3 实现灾害效果（例如：增加水消耗）。
- [ ] 7.4 创建 `DisasterAlert` UI 组件。

## 8. Population & Polish (人口与打磨)

- [ ] 8.1 实现基础人口增长逻辑。
- [ ] 8.2 添加“昼/夜”循环或仅天数推进。
- [ ] 8.3 添加游戏结束条件（例如：人口 = 0）。