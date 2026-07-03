# Release Notes / Options Level Pro 2.0.1 / ATAS X

This is a stable Options Level Pro 2.0.1 release package for ATAS X.
这是适用于 ATAS X 的 Options Level Pro 2.0.1 稳定发布包。

## Added / 新增

- Added the ``0DTE Options Exposure Heatmap`` for ES, MES, NQ, and MNQ charts. MES uses ES heatmap data, and MNQ uses NQ heatmap data.
- 新增适用于 ES / MES / NQ / MNQ 图表的 ``0DTE Options Exposure Heatmap``，其中 MES 复用 ES 热图数据，MNQ 复用 NQ 热图数据。
- The heatmap reads only 0DTE key-level exposure values from the protected TradingHub data path.
- 热图仅通过 TradingHub 受保护数据链路读取 0DTE 关键位敞口数据。
- Added heatmap settings for labels, opacity, line height, minimum width, and main colors.
- 新增热图标签、透明度、线条高度、最小宽度和主要颜色设置。
- Unified the ATAS X release-package version number at ``2.0.1``.
- ATAS X 发布包版本号统一为 ``2.0.1``。

## Changed

- Static options level lines are retained.
- 保留静态期权关键位水平线。
- Visible names use professional TradingHub options terminology without exposing upstream labels verbatim.
- 用户可见名称使用 TradingHub 专业期权术语，不逐字暴露上游标签。
- Provides a separate ATAS X DLL archive.
- 提供独立的 ATAS X DLL 归档。
- The native heatmap core is embedded into the indicator DLL for single-DLL installation.
- 原生期权热图核心已内嵌到指标 DLL，安装时只需要一个 DLL。
- The server keeps the short 0DTE heatmap cache, while the indicator syncs the current server window once and then requests only new snapshots.
- 服务端保留短期 0DTE 热图缓存，指标端首次同步当前服务器窗口，之后只请求新增快照。

## Note

Download the DLL that matches your ATAS version. Do not mix DLLs across ATAS versions.
请下载与 ATAS 版本匹配的 DLL，不要混用不同 ATAS 版本的 DLL。
