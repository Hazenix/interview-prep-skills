# React 专项考察

仅在 `framework_scope=react` 或 `both` 时读取。结合候选人项目、React 版本和运行方式选题。只问一个问题，答案证据记为 `react:*`；不要以背诵 Fiber 内部字段、某版调度细节或“所有更新都异步”等口号判断能力。

| 场景或主问题 | 可靠回答应涉及 | 下一层追问 |
|---|---|---|
| 列表重排后输入框的值跑到另一行，先查什么？ | `key` 与组件身份、稳定业务 ID、位置变化和状态保留 | 为什么数组索引在可重排列表中可能出问题？ |
| 连续两次 `setCount(count + 1)` 的结果和预期不同，怎么解释？ | 当前渲染的 state 快照、批处理语境、函数式更新 | 异步回调读到旧值时如何处理？ |
| `useEffect` 发请求时快速切换用户，页面出现旧数据，怎么改？ | effect 依赖、cleanup、取消或忽略过期结果、竞态验证 | 请求已返回但组件已卸载时，怎样避免写入旧状态？ |
| 一个计算值被放进 state 和 effect，导致同步困难，怎样简化？ | 派生值可在渲染阶段计算；真正与外部系统同步才用 effect | 计算很贵时如何测量再决定是否 memoize？ |
| 子组件频繁重渲染导致卡顿，怎样证明原因？ | React Profiler、状态归属、props 身份、memo 的适用条件与成本 | `memo` 为什么不能阻止自身 state 更新？ |
| 表单输入有时被重置，怎么定位？ | 受控/非受控输入、组件身份、`key`、状态归属 | 在切换 Tab 时是否要保留草稿，怎样决定？ |
| 组件库需要复用数据加载逻辑，怎样设计 Hook？ | Hook 规则、输入输出、状态/错误/清理契约、测试 | 两个组件调用同一个自定义 Hook，会自动共享 state 吗？ |
| 项目用了 SSR 或 Next.js，首屏与 hydration 异常如何排查？ | 服务器/客户端输出差异、环境依赖、数据与版本、浏览器控制台证据 | 哪些内容只在客户端可用？ |

评分优先看候选人能否解释实际 UI 行为、定位证据和修复边界。`useEffect`、memo、渲染与 hydration 的行为需结合 React 与框架版本；开发模式的额外检查不等于生产环境执行次数。

官方核对入口：[React State as a Snapshot](https://react.dev/learn/state-as-a-snapshot)、[Rendering Lists](https://react.dev/learn/rendering-lists)、[Synchronizing with Effects](https://react.dev/learn/synchronizing-with-effects)、[You Might Not Need an Effect](https://react.dev/learn/you-might-not-need-an-effect)。
