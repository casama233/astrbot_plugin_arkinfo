# ark_info_search — Arknights PRTS Wiki Lookup

[简体中文](README.md) · [繁體中文](README.zh-TW.md) · **English**

An AstrBot plugin adapted from [wxgl/astrbot_plugin_arkinfo](https://github.com/wxgl/astrbot_plugin_arkinfo) to query Arknights information via PRTS Wiki's MediaWiki API. The inherited upstream README notes limited development time and some AI-assisted code.

**Limitations:** Pages with images may load slowly, and operator-info lookups can sometimes fail.

## Features

- Query the [PRTS Wiki](https://prts.wiki/w/%E9%A6%96%E9%A1%B5) via its [MediaWiki API](https://prts.wiki/api.php).
- Retrieve some operator artwork, enemy images and stage-map image links.
- Several features are unfinished and should not be treated as production-complete.

## Project structure

| File / module | Purpose |
| --- | --- |
| `search_model.py` | Most MediaWiki API requests |
| `ganyuan.py` | Operator information (partial coverage) |
| `other_thing.py` | Other information (unfinished) |
| `__main__.py` | Entry point using relative imports |
| `gongzhao.py` | Recruitment information |
| `stage_enemy.py` | Stage enemy statistics |
| `data/enemy_data.json` | Stored enemy names |

## Dependencies

`httpx`, `asyncio`, and `beautifulsoup4`. Confirm compatibility with your AstrBot and Python installation before deploying.

## Contributions and roadmap

Bug reports, suggestions and pull requests are welcome. Planned work includes **configuration settings** and **material queries**.

## Upstream and license

This repository is a fork of [wxgl/astrbot_plugin_arkinfo](https://github.com/wxgl/astrbot_plugin_arkinfo). Upstream uses **AGPL-3.0**, and all applicable copyright and license notices must be preserved. This fork does not claim to have newly authored upstream code or extend licenses to third-party content, data or dependencies.
