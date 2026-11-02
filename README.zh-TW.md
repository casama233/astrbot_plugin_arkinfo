# ark_info_search — 明日方舟 PRTS 查詢

[简体中文](README.md) · **繁體中文** · [English](README.en.md)

此專案基於 [wxgl/astrbot_plugin_arkinfo](https://github.com/wxgl/astrbot_plugin_arkinfo) 改編，目的是讓 AstrBot 使用 PRTS Wiki 的 MediaWiki API 查詢《明日方舟》資訊。上游說明指出開發時間有限且部分程式碼借助 AI 完成。

**注意：** 帶圖片的資料載入速度可能較慢，幹員資訊查詢偶爾會失敗。

## 功能

- 從 [PRTS Wiki](https://prts.wiki/w/%E9%A6%96%E9%A1%B5) 查詢資料。
- 使用 [PRTS MediaWiki API](https://prts.wiki/api.php)。
- 已有部分圖片連結查詢能力：幹員立繪、敵人圖片與關卡地圖；整體功能仍不完整。

## 專案結構

| 檔案／模組 | 用途 |
| --- | --- |
| `search_model.py` | 大部分 MediaWiki API 請求 |
| `ganyuan.py` | 幹員資訊（僅部分可查） |
| `other_thing.py` | 其他資訊（待完善） |
| `__main__.py` | 使用相對匯入的程式入口 |
| `gongzhao.py` | 公開招募資訊 |
| `stage_enemy.py` | 關卡敵人數值 |
| `data/enemy_data.json` | 敵人名稱資料 |

## 相依

`httpx`、`asyncio`、`beautifulsoup4`。安裝前請檢查目前 AstrBot 與 Python 環境的相容性。

## 參與及待辦

歡迎提出 Bug 回報、功能建議及 Pull Request。目前待辦包括**配置設定**及**材料查詢**。

## 上游來源與授權

本倉庫是 [wxgl/astrbot_plugin_arkinfo](https://github.com/wxgl/astrbot_plugin_arkinfo) 的 fork。上游採 **AGPL-3.0**，相關許可及著作權聲明必須保留。本分支不聲稱上游作品為重新創作，亦不把本倉庫的許可擴張至第三方素材、資料或依賴。
