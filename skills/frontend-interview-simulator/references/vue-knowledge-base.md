# Vue 专项考察

仅在 `framework_scope=vue` 或 `both` 时读取。先确认 Vue 版本及 Options API、Composition API 或 `<script setup>` 的实际用法。答案证据记为 `vue:*`；不能把 Vue 2 与 Vue 3 的响应式实现混为一谈。

| 场景或主问题 | 可靠回答应涉及 | 下一层追问 |
|---|---|---|
| 解构 `reactive` 对象后模板不再更新，怎么解释？ | 访问响应式代理的方式、解构后的绑定、`toRefs`/`toRef` 等可选方案 | `ref` 解构和 `reactive` 属性解构有什么不同？ |
| 某个派生结果写在 `watch` 中，状态容易不同步，怎么调整？ | `computed` 适合纯派生，`watch` 适合副作用；依赖与缓存语义 | 异步请求为何不能直接当作普通 computed 值？ |
| 快速切换搜索条件，旧请求结果覆盖新结果，怎么处理？ | watch 来源、清理或取消、过期结果隔离、错误状态 | 组件卸载时还需要清理什么？ |
| 列表重排后子组件状态错位，先查什么？ | 稳定 `key`、VNode 身份、局部 state 与重排 | 哪些情况下索引 key 会掩盖问题？ |
| 子组件修改父组件数据后行为难以追踪，怎么整理？ | props 向下、事件或模型更新向上、共享状态的范围 | 组件库的双向绑定 API 如何定义边界？ |
| 大表格滚动卡顿，怎么定位？ | 渲染数量、响应式追踪、虚拟列表适用性、性能分析证据 | 虚拟列表会给键盘导航带来什么影响？ |
| 项目用了 Nuxt 或 SSR，hydration 不一致如何排查？ | 服务端与客户端输出一致性、仅浏览器可用 API、数据与版本 | 哪些状态需要在首屏服务端与客户端保持一致？ |

只要求解释可观察行为、所用版本的语义和验证办法，不要求背内部依赖收集的数据结构。对 `watch` 的执行时机或清理 API 先核对目标 Vue 版本。

官方核对入口：[Vue Reactivity Fundamentals](https://vuejs.org/guide/essentials/reactivity-fundamentals)、[Computed Properties](https://vuejs.org/guide/essentials/computed)、[Watchers](https://vuejs.org/guide/essentials/watchers)、[List Rendering](https://vuejs.org/guide/essentials/list)。
