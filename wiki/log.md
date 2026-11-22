---
title: 紀錄
type: log
---

# 操作紀錄

> 只往後追加。格式：`## [YYYY-MM-DD] <ingest|query|lint|edit|schema> | 標題`

## [2026-11-22] schema | 建立 wiki 骨架
- 建立 AGENTS.md、CLAUDE.md、templates/（7 種範本）
- 建立 wiki/index.md、wiki/log.md、wiki/overview.md
- 主題：地球與自然；預設批次 ingest；Query 存回前先問

## [2026-11-22] schema | 紅線：刪檔前必須先問
- AGENTS.md 第 2 節第 3 條改為：刪除任何檔案前必須先問過使用者，不得擅自刪除
- Lint 的機械性修正也不包含刪檔

## [2026-11-22] ingest | 第一批：NOAA／NASA／USGS 公開資料（7 份）
- 取得方式：使用者要求「上網找公開資料」；LLM 讀取美國政府公開網頁（public domain），整理成英文筆記存入 raw/（capture: llm-notes）
- 無法取得：USGS《This Dynamic Earth》（HTTP 403），改用 NOAA 兩篇板塊短文
- 新建來源：[[src-noaa-plate-boundaries|NOAA：板塊邊界與板塊移動]]、[[src-noaa-water-cycle|NOAA：水循環]]、[[src-noaa-atmosphere-layers|NOAA JetStream：大氣分層與組成]]、[[src-nasa-carbon-cycle|NASA Earth Observatory：碳循環]]、[[src-noaa-ocean-currents|NOAA：洋流]]、[[src-usgs-ice-glaciers|USGS：冰、雪與冰川]]、[[src-noaa-coral-reefs|NOAA：珊瑚礁生態系]]
- 新建概念：[[plate-tectonics|板塊構造]]、[[water-cycle|水循環]]、[[atmosphere-layers|大氣分層]]、[[greenhouse-effect|溫室效應]]、[[carbon-cycle|碳循環]]、[[ocean-currents|洋流]]、[[ocean-acidification|海洋酸化]]、[[glaciers-and-ice-sheets|冰川與冰蓋]]、[[coral-reef|珊瑚礁]]
- 新建地點：[[greenland-ice-sheet|格陵蘭冰蓋]]、[[gulf-stream|墨西哥灣流]]
- 新建事件：[[last-glacial-period|末次冰期]]、[[global-coral-bleaching-2014-2017|2014–2017 全球珊瑚白化事件]]
- 更新：[[index|目錄]]、[[overview|總綜述]]
- 矛盾：
  - 冰佔地球總水量 1.7% vs 2.1%（USGS 兩頁）→ 暫採 1.7%（可由體積表驗算）
  - 末次冰期結束 1.8 萬 vs 2 萬年前（USGS）vs 1 萬年前（NASA）→ 判斷為不同時間點，待古氣候來源確認
  - 海水比例 97.5% / 97% / 96.5%（NOAA 同頁）→ 定義不同，非矛盾
  - 岩石圈定義、板塊數量（NOAA 兩篇）→ 採「地殼 + 上部地函」
- 過時：NASA 碳循環數據多為 2005–2010 年

## [2026-11-22] edit | 收錄範圍：岩石圈暫停、生物圈只收珊瑚礁
- 使用者決定：岩石圈暫不收錄新資料；生物圈暫時只收錄珊瑚礁
- 更新：[[overview|總綜述]]（新增「收錄範圍」段落，知識缺口改標暫緩）

## [2026-11-22] ingest | 第二批：補齊知識缺口（13 份來源）
- 範圍：依使用者「將缺失資料都補齊」，在收錄範圍內（岩石圈暫停、生物圈只收珊瑚礁）補齊缺口
- 無法取得：NOAA Climate.gov 海平面／CO₂／氣溫／AMOC（403）、大英百科（403）、中央氣象署氣候百科（404）、NCDR 與台師大梅雨 PDF（無法擷取文字）、中研院黑潮海報（檔案過大）、台大黑潮論文（連線中斷）、海保署珊瑚報告 PDF（未讀取）；均改用替代來源或列為缺口
- 新建來源：[[src-noaa-coral-tutorial|NOAA 珊瑚教學]]、[[src-noaa-coral-bleaching|NOAA 珊瑚白化]]、[[src-taiwan-coral-reports|台灣珊瑚報導]]、[[src-noaa-ocean-acidification|NOAA 海洋酸化]]、[[src-noaa-nasa-co2-temperature-2026|NOAA／NASA 最新 CO₂ 與氣溫]]、[[src-nasa-noaa-sea-level|NASA／NOAA 海平面]]、[[src-nsidc-ice-sheets|NSIDC 冰蓋]]、[[src-nsidc-sea-ice-permafrost|NSIDC 海冰與永凍土]]、[[src-noaa-gyres-gulf-stream|NOAA 環流圈與灣流]]、[[src-kuroshio-jma-wikipedia|黑潮資料]]、[[src-amoc-noaa-wikipedia|AMOC 資料]]、[[src-wikipedia-last-glacial|維基：末次冰期]]、[[src-wikipedia-east-asian-monsoon|維基：東亞季風]]
- 新建概念：[[sea-level-rise|海平面上升]]、[[sea-ice|海冰]]、[[permafrost|永凍土]]、[[amoc|大西洋經向翻轉環流]]、[[east-asian-monsoon|東亞季風與梅雨]]
- 新建地點：[[antarctic-ice-sheet|南極冰蓋]]、[[kuroshio|黑潮]]、[[taiwan-coral-reefs|台灣的珊瑚礁]]
- 新建事件：[[global-coral-bleaching-2023-2025|2023–2025 全球珊瑚白化事件]]
- 更新：[[coral-reef|珊瑚礁]]（大幅改寫）、[[ocean-acidification|海洋酸化]]（大幅改寫）、[[carbon-cycle|碳循環]]、[[greenhouse-effect|溫室效應]]、[[atmosphere-layers|大氣分層]]、[[water-cycle|水循環]]、[[ocean-currents|洋流]]、[[glaciers-and-ice-sheets|冰川與冰蓋]]、[[greenland-ice-sheet|格陵蘭冰蓋]]、[[gulf-stream|墨西哥灣流]]、[[last-glacial-period|末次冰期]]、[[global-coral-bleaching-2014-2017|2014–2017 白化事件]]、[[index|目錄]]、[[overview|總綜述]]
- 新矛盾：
  - 第三次白化影響範圍 70%（NOAA 教學頁）vs 68.2%（Coral Reef Watch）→ 採 68.2%
  - 格陵蘭冰蓋體積 250 萬 km³（USGS）vs 290 萬 km³（NSIDC）→ 採 NSIDC
  - 海平面上升速率 4.4 mm/年（NASA，目前）vs 3.2 mm/年（NOAA，未註明期間）→ 判斷為最新值與長期平均之差
  - 黑潮寬度約 100 km（JMA、英文維基）vs 200 多 km（中文維基）→ 採 100 km
  - 灣流起點：加勒比海 vs 墨西哥灣（兩份 NOAA）→ 判斷為描述範圍不同
  - 全球造礁珊瑚 1,600 多種（新聞）vs 硬珊瑚約 800 種（NOAA）→ 暫以 NOAA 為準
- 舊矛盾更新：末次冰期結束時間 → 依維基時間軸判斷三個數字分別指消冰開始與冰期結束，待使用者確認
- 過時數據已更新：CO₂ 387 ppm（2011 文）→ 427.35 ppm（2025 年平均）

## [2026-11-22] edit | 使用者裁定：採用 LLM 對各組矛盾的判斷
- 使用者表示「先照你的判斷」；依 AGENTS.md 第 6 節，把「說法不一致」callout 改為簡短的「已裁定」註記
- 涉及頁面：[[glaciers-and-ice-sheets|冰川與冰蓋]]（1.7%）、[[plate-tectonics|板塊構造]]（岩石圈定義、板塊數量）、[[water-cycle|水循環]]（海水比例）、[[global-coral-bleaching-2014-2017|2014–2017 白化]]（68.2%）、[[last-glacial-period|末次冰期]]（時間點）、[[greenland-ice-sheet|格陵蘭冰蓋]]（290 萬 km³）、[[gulf-stream|墨西哥灣流]]（起點）、[[kuroshio|黑潮]]（100 km）、[[src-nasa-noaa-sea-level|海平面資料]]（速率）、[[src-taiwan-coral-reports|台灣珊瑚報導]]與[[taiwan-coral-reefs|台灣的珊瑚礁]]（珊瑚種數）
- 使用者用「先」，表示日後有更好的來源時可以重新檢討

## [2026-11-22] lint | 第一次健康檢查
- 檢查 45 頁：無斷連、無孤兒頁、無缺欄位、raw/ 全部已收錄、index 與檔案一致、各頁之間沒有發現新的矛盾
- 已直接修正（機械性）：
  - 7 頁 frontmatter 的 sources 與內文引用不一致 → 補上或移除（[[atmosphere-layers|大氣分層]]、[[east-asian-monsoon|東亞季風與梅雨]]、[[sea-level-rise|海平面上升]]、[[global-coral-bleaching-2023-2025|2023–2025 白化]]、[[taiwan-coral-reefs|台灣的珊瑚礁]]、[[carbon-cycle|碳循環]]、[[ocean-acidification|海洋酸化]]）
  - 約 25 行數據補上來源連結（珊瑚礁、冰川、大氣分層、碳循環、海冰、永凍土等 13 頁）
  - [[index|目錄]] 的來源數同步更新
- 未修正，待使用者決定：
  - 本檔第一筆 ingest 紀錄有 22 個沒有顯示文字的連結；log 規定只能往後追加，與「連結一律用顯示文字」衝突
- 建議新頁：聖嬰現象、颱風、冰芯、冰棚（各被 4 頁提到但沒有專頁）
- 圈層分布：水圈 16、大氣圈 8、冰凍圈 8、生物圈 7（只收珊瑚礁）、岩石圈 3（暫停）
- 仍過時：[[carbon-cycle|碳循環]]中 2009 年的排放數字（缺最新全球排放量）

## [2026-11-22] edit | 補上 log 舊紀錄的連結顯示文字
- 使用者決定直接修正：第一批 ingest 紀錄的 22 個裸連結補上中文顯示文字（只改格式，不改紀錄內容）

## [2026-11-22] query | 製作教學型 HTML 簡報「認識我們的星球」
- 產出：slides/earth-intro.html（21 頁，給不熟悉主題的入門者；單一 HTML 檔，可離線開啟）
- 內容只取自 wiki：五大圈層、[[plate-tectonics|板塊構造]]、[[water-cycle|水循環]]、[[atmosphere-layers|大氣分層]]、[[greenhouse-effect|溫室效應]]、[[carbon-cycle|碳循環]]、[[ocean-currents|洋流]]、[[amoc|大西洋經向翻轉環流]]、[[glaciers-and-ice-sheets|冰川與冰蓋]]、[[sea-ice|海冰]]、[[permafrost|永凍土]]、[[sea-level-rise|海平面上升]]、[[last-glacial-period|末次冰期]]、[[coral-reef|珊瑚礁]]、[[ocean-acidification|海洋酸化]]、[[kuroshio|黑潮]]、[[east-asian-monsoon|東亞季風與梅雨]]、[[taiwan-coral-reefs|台灣的珊瑚礁]]
- 圖表 4 張（淡水去處、CO₂ 年平均、冰蓋海平面當量、全球白化事件），附數據表；另有課後練習與參考答案
- 標示為「比喻」的內容為輔助理解的近似說法，不是 wiki 中的事實
- 未存回 wiki（簡報是輸出物，不是知識頁）

## [2026-11-22] edit | 簡報改版：自然科學探索風格、全螢幕互動式
- 檔案：slides/earth-intro.html（內容與數據不變，仍只取自 wiki）
- 版面：上方章節名稱與分段進度條、中間主內容、下方上一頁／下一頁（顯示前後頁標題）、右側章節快速導覽；窄螢幕時導覽收進「☰ 章節」按鈕
- 視覺：8 章各有一幅以 SVG 繪製的自然場景背景（太空中的地球、山脈、天空與海洋、森林、深海、冰川、珊瑚礁、黎明島嶼），深藍／淺藍／綠配色、半透明資訊卡片
- 動畫：背景緩慢推近、內容淡入上浮、章節切換標題、圖表長條生長與折線描繪；支援「減少動態」設定
- 互動：水循環頁可逐步點選「蒸發 → 凝結 → 降水 → 逕流與入滲」或自動播放；課後練習改成點開看提示
- 背景為示意插畫，不是照片，也不是 wiki 來源

## [2026-11-22] edit | 作業規格書與簡報數字可追溯檢查
- 新增：assignment-spec.md（課堂作業規格書：Wiki 介紹、成果、簡報規格、loop／graph 設計、執行紀錄、反思）
- 檢查：用腳本比對簡報上 95 個數字是否都出現在 wiki，發現 3 個只存在於 raw/（CO₂ 2020 年 414.21、2021 年 416.41、2023 年 421.08 ppm）
- 更新：[[src-noaa-nasa-co2-temperature-2026|NOAA／NASA：最新 CO₂ 與氣溫]] 補上 1959、2019–2025 完整年平均序列（出處為同一份 raw）；重新比對後全部可追溯
- 重新跑 lint：結構檢查全部通過；「無出處數字」6 筆經人工確認為誤判

## [2026-11-22] edit | 刪除 assignment-spec.md（經使用者同意）
- 原因：使用者要求規格書不放在專案資料夾，改做成 Word 檔另外提供（存放於資料夾外）
- 刪除：assignment-spec.md（上一筆紀錄新增的檔案）；wiki 中沒有其他頁面連到它
- 上一筆紀錄的內容依「只往後追加」原則保留不改，以本筆說明後續變動
