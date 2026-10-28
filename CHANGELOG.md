# Changelog

## 0.1.4

- feat: SmartTree 新增 `expandSelectedPath`——按节点 key 链展开定位（左树统一收口，四树默认全折叠）
- feat: 数据层懒加载支持——树组件配合宿主 loadData 通道按库拉取（admin 知识库页首屏 3-5s 根治的组件侧）
- fix: 测试集树排序改编号优先（端到端评测组 1→9 归位）
- chore: 许可统一 MIT


## v0.1.3

- perf: package.json 声明 `sideEffects` 仅样式文件（`**/*.css` / `**/*.less` / `**/styles/**`）——组件模块可被消费方 bundler tree-shake，此前未声明时打包器保守保留整个库（docs-ui / sop-ui / evals-ui / ui-kit 的树组件均依赖本包）
- ci: package.json 无 BOM 断言（发版改版本号时容易带入 BOM，vendored 引用会解析失败）

## v0.1.2

- feat: npm registry 正式上架（@angineer/smartree）

## v0.1.0

- 通用树组件 SmartTree 独立发布（搜索、拖拽、文件上传、状态标签、暗色模式）
- 搜索高亮 XSS 修复、去除 JSON 深拷贝、主题变量默认值、无障碍操作按钮、虚拟滚动透传
- 组件泛型化（`T extends SmartTreeNode`），提供组树/排序工具（`buildTreeFromFlat` / `sortTreeNodes`）
