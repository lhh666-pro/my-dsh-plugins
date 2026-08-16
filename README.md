# my-dsh-plugins

DeepSeek Harness Web 插件集（个人维护）。

## 插件列表

| 插件 | 说明 |
| --- | --- |
| [dsh-session-archive](./packages/dsh-session-archive) | 会话归档管理：查看已归档/全部会话，一键**取消归档**恢复侧栏，两步确认永久删除 |

## 安装

以 `dsh-session-archive` 为例（每个插件包内 README 有各自说明）：

1. 将 `packages/<插件名>` 复制到 DSH 的 `data/profiles/node_modules/@local/` 下
2. 在 `data/profiles/web/cordis.patch.yml` 注册对应插件行（见各包内 `cordis.patch.yml`）
3. 重启 DSH Web 生效

## 开发

- 宿主半：`lib/index.js`（Node.js / Cordis 插件）
- 客户端半：`lib/client.js`（浏览器 / ModuleLoader 格式）
- 每个插件是独立标准包：`package.json` + `cordis.patch.yml` + `lib/`

## License

MIT
