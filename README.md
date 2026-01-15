# grafana-demo
Grafana 的 Demo 專案

## 簡介
本專案提供了一個完整的監控解決方案演示，整合了 **Grafana**, **Prometheus**, **Loki** 和 **Promtail**。
旨在展示如何快速搭建一個具備指標監控與日誌聚合功能的觀測平台。

主要組件：
- **Grafana**: 視覺化儀表板與分析平台。
- **Prometheus**: 系統監控與報警工具包，負責收集指標。
- **Loki**: 類似 Prometheus 的日誌聚合系統，但專為日誌設計。
- **Promtail**: 代理端，負責收集日誌並發送給 Loki。
- **Node Exporter**: 用於導出硬體和操作系統指標。

## Docker Compose 配置
本專案使用 `docker-compose.yml` 定義了以下服務：

| 服務名稱 | 描述 | 端口映射 |
| :--- | :--- | :--- |
| **grafana** | Web 介面與儀表板 | `3000` |
| **prometheus** | 指標收集與查詢 | `9090` |
| **loki** | 日誌聚合系統 | `3100` |
| **promtail** | 日誌收集代理 | - |
| **node_exporter** | 主機指標導出 | `9100` |

## 啟動
```bash
docker compose up -d

# 停止
docker compose down
```

## 檢查
```bash
docker compose ps
```

## 登入網頁
http://localhost:3000
預設帳密: admin/admin

