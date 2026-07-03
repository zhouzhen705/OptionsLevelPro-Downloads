# Release Notes / Options Level Pro 2.0.8 / ATAS X

This is a stable Options Level Pro 2.0.8 release package for ATAS X.
这是适用于 ATAS X 的 Options Level Pro 2.0.8 稳定发布包。

## Added / 新增

- Added local Options Level Pro data storage under `%APPDATA%\ATAS\OLP` for static levels and 0DTE heatmap snapshots.
- 新增 `%APPDATA%\ATAS\OLP` 本地数据目录，用于保存静态关键位和 0DTE 热图快照。
- Added a heatmap display-window setting. It limits the chart display range without deleting saved local history.
- 新增热图显示窗口设置，只限制图表显示范围，不删除已保存的本地历史数据。
- Added same-day server history sync for the 0DTE Options Exposure Heatmap.
- 新增 0DTE Options Exposure Heatmap 当天服务器 history 同步。
- Unified the ATAS X release-package version number at `2.0.8`.
- ATAS X 发布包版本号统一为 `2.0.8`。

## Changed / 更新

- Static options level lines are retained.
- 保留静态期权关键位水平线。
- The indicator reads saved local heatmap data first, then polls only new snapshots from the protected TradingHub data path.
- 指标会先读取本地已保存热图数据，再通过 TradingHub 受保护数据链路只轮询新增快照。
- Static-level sync writes returned ES and NQ history to the local cache together.
- 静态关键位同步会把返回的 ES 和 NQ 历史一并写入本地缓存。
- If the server static-level date is earlier than the current ET date but valid ES / NQ levels are available, the indicator keeps showing the latest available data with its date label.
- 当服务器静态关键位日期早于当前 ET 日期但仍返回有效 ES / NQ levels 时，指标继续显示最新可用数据并标注数据日期。
- From 03:00 to 03:05 ET, static levels are force-refreshed every 30 seconds.
- 美东时间 03:00 至 03:05 会每 30 秒强制刷新静态关键位。
- The heatmap reads current-day server history once, then uses incremental polling for new snapshots.
- 热图会先读取当天服务器 history，随后继续使用增量轮询获取新增快照。
- ES and NQ heatmap snapshots are stored together locally. MES uses ES data, and MNQ uses NQ data.
- ES 和 NQ 热图快照会一并保存在本地；MES 复用 ES 数据，MNQ 复用 NQ 数据。
- Visible names use professional TradingHub options terminology without exposing upstream labels verbatim.
- 用户可见名称使用 TradingHub 专业期权术语，不逐字暴露上游标签。
- Provides a separate ATAS X DLL archive.
- 提供独立的 ATAS X DLL 归档。
- The native heatmap core is embedded into the indicator DLL for single-DLL installation.
- 原生期权热图核心已内嵌到指标 DLL，安装时只需要一个 DLL。
- The 0DTE heatmap collapses consecutive duplicate snapshots before cache reads, merges, writes, and chart rendering.
- 0DTE 热图会在读取、合并、写入缓存和图表绘制前压缩连续重复快照。
- Chart rendering now draws per-key linear timelines to reduce lag with high-frequency intraday history.
- 图表绘制改为按 key 线性时间线渲染，降低高频盘中 history 导致的卡顿。
- Heatmap cache writes now use compact JSON to reduce local cache size and future read overhead.
- 热图缓存写入改为紧凑 JSON，降低本地缓存文件体积和后续读取负担。
- The 0DTE heatmap fetches, caches, merges, and renders snapshots only during weekdays 09:30-16:30 ET.
- 0DTE 热图只在美东时间工作日 09:30-16:30 拉取、缓存、合并和绘制快照。
- Heatmap line segments are capped at 16:30 ET and no longer extend into after-hours or overnight chart areas.
- 热图线段会在当天 16:30 ET 截断，不再延伸到盘后或隔夜图表区域。
- The heatmap refresh interval is fixed at 10 seconds and is no longer exposed as a user setting.
- 热图刷新间隔固定为 10 秒，不再作为用户可调整设置显示。
- Added a separate 0DTE heatmap status text line below the static-data status text.
- 在静态数据状态文字下方新增独立的 0DTE 热图状态文字。
- Added a user setting to show or hide the heatmap status text without changing heatmap rendering.
- 新增热图状态文字显示开关，可独立控制文字提示，不影响热图绘制。
- The latest intraday 0DTE heatmap segment extends into the right-side chart area while waiting for the next candle.
- 盘中最新 0DTE 热图段会在等待下一根 K 线时延伸到图表右侧空白区域。
- After-hours and historical sessions remain capped at 16:30 ET.
- 盘后和历史日期仍按当天 16:30 ET 截断。

## Note

Download the DLL that matches your ATAS version. Do not mix DLLs across ATAS versions.
请下载与 ATAS 版本匹配的 DLL，不要混用不同 ATAS 版本的 DLL。
