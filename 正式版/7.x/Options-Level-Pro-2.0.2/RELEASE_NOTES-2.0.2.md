# Release Notes / Options Level Pro 2.0.2 / ATAS 7.x

This is a stable Options Level Pro 2.0.2 release package for ATAS 7.x.
这是适用于 ATAS 7.x 的 Options Level Pro 2.0.2 稳定发布包。

## Added / 新增

- Added local Options Level Pro data storage under ``%APPDATA%\ATAS\OLP`` for static levels and 0DTE heatmap snapshots.
- 新增 ``%APPDATA%\ATAS\OLP`` 本地数据目录，用于保存静态关键位和 0DTE 热图快照。
- Added a heatmap display-window setting. It limits the chart display range without deleting saved local history.
- 新增热图显示窗口设置，只限制图表显示范围，不删除已保存的本地历史数据。

## Changed

- Static options level lines are retained.
- 保留静态期权关键位水平线。
- The indicator reads saved local heatmap data first, then polls only new snapshots from the protected TradingHub data path.
- 指标会先读取本地已保存热图数据，再通过 TradingHub 受保护数据链路只轮询新增快照。
- Static-level sync writes returned ES and NQ history to the local cache together.
- 静态关键位同步会把返回的 ES 和 NQ 历史一并写入本地缓存。
- ES and NQ heatmap snapshots are stored together locally. MES uses ES data, and MNQ uses NQ data.
- ES 和 NQ 热图快照会一并保存在本地；MES 复用 ES 数据，MNQ 复用 NQ 数据。
- Visible names use professional TradingHub options terminology without exposing upstream labels verbatim.
- 用户可见名称使用 TradingHub 专业期权术语，不逐字暴露上游标签。
- Provides a separate ATAS 7.x DLL archive.
- 提供独立的 ATAS 7.x DLL 归档。
- The native heatmap core is embedded into the indicator DLL for single-DLL installation.
- 原生期权热图核心已内嵌到指标 DLL，安装时只需要一个 DLL。

## Note

Download the DLL that matches your ATAS version. Do not mix DLLs across ATAS versions.
请下载与 ATAS 版本匹配的 DLL，不要混用不同 ATAS 版本的 DLL。
