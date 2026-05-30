# 🎬 Retro Animation Studio Pro (v3.0)

> **gifshot 라이브러리 탑재로 완성된 고품질 웹 애니메이션 스튜디오**
> 
> 본 프로젝트는 기존 자작 LZW 엔진의 한계를 극복하고, 외부 라이브러리(`gifshot`)를 도입하여 실시간 멀티스레딩 연산 및 256색 고해상도 양자화 출력을 구현한 고기능 애니메이션 제작 도구입니다.
>
> This project is a highly functional animation creation tool that overcomes the limitations of previous custom LZW engines by integrating the external library `gifshot`, enabling real-time multi-threaded processing and high-resolution 256-color quantization output.

---

## ✍️ 작성인 / Authors / 制作・開発 / 作者 / Mga May-akda
이 프로젝트의 설계, 아키텍처 개선 및 코드 고도화는 다음 두 AI 협업 모델의 공동 작업으로 작성되었습니다.
This project's design, architectural improvement, and code optimization were created through the collaborative work of the following two AI models:

* **Gemini (제미나이 / ジェミニ / 双子座 / Hiyas)**
* **ChatGPT (챗지피티 / チャットGPT / 聊天GPT)**

---

## 🌐 Multi-language README Navigation
* [한국어 (Korean)](#-한국어-korean)
* [English (영어)](#-english-영어)
* [日本語 (Japanese)](#-日本語-japanese)
* [简体中文 (Simplified Chinese)](#-简体中文-simplified-chinese)
* [Tagalog / Filipino (필리핀어)](#-tagalog--filipino-필리핀어)

---

## 🇰🇷 한국어 (Korean)

### 🚀 주요 개선 사항 (Changelog v3.0)
기존 순수 자바스크립트(Vanilla JS) 기반 엔진에서 **외부 전문 라이브러리 체제**로 전면 전환하면서 다음과 같은 치명적인 한계들을 해결했습니다.
* **고품질 색상 보정 (256 Color Quantization):** 기존 16색 제한을 해제하고 256색 팔레트 추출 및 디더링을 지원하여 파스텔톤, 에어브러시 효과, 미세한 그라데이션이 깨짐 없이 선명하게 출력됩니다.
* **비동기식 멀티스레드 연산 (Web Workers):** GIF 인코딩이 메인 UI 스레드가 아닌 백그라운드 멀티스레드에서 실행되므로, 프레임이 많아도 브라우저가 멈추거나 먹통이 되지 않고 실시간 진행률(%)이 표시됩니다.
* **압축률 최적화:** LZW 사전(Dictionary) 빌드 최적화 표준 규격을 준수하여 최종 GIF 파일 용량이 이전 대비 수 배 이상 획기적으로 감소합니다.

### ✨ 핵심 기능 (Features)
* **레이어 시스템:** 총 5개의 독립된 레이어(`L1` ~ `L5`) 지원 및 개별 선택 제어
* **멀티 브러시 프리셋:** 속도 감응형 압력을 지원하는 펜(Pen), 스케치용 연필(Sketch), 입자 분사식 에어브러시(Airbrush)
* **어니언 스킨 (Onion Skin):** 전/후 프레임을 불투명도 및 색상 가이드(Red/Green)로 시각화하는 지능형 라이트박스 모드
* **실시간 미니 플레이어:** 편집 중인 애니메이션을 우측 상단 윈도우에서 무한 루프로 상시 프리뷰 제공
* **프로페셔널 내보내기 (Export):** `gifshot` 연동 고품질 GIF 다운로드, 프레임별 PNG 시퀀스 다운로드, 게임 엔진용 컴포지트 스프라이트 시트(Sprite Sheet) 생성

### 💻 실행 방법 (How to Run)
1. 소스코드를 `index.html` 파일로 저장합니다.
2. 브라우저(Chrome, Edge, Safari 등)에서 해당 파일을 실행합니다.
3. 좌측 툴바와 상단 팔레트를 이용해 그림을 그린 뒤, 하단 `➕ Add Frame` 버튼으로 타임라인을 확장합니다.
4. 작업이 완료되면 좌측 상단의 `🎬 Export High-Q GIF` 메뉴를 클릭하여 다운로드합니다.

---

## 🇺🇸 English (영어)

### 🚀 Major Improvements (Changelog v3.0)
By transitioning from the legacy pure JavaScript (Vanilla JS) engine to an **external specialized library architecture**, the following critical bottlenecks have been resolved:
* **High-Quality Color Correction (256 Color Quantization):** The previous 16-color limitation has been removed. It now supports 256-color palette extraction and dithering, ensuring pastel tones, airbrush effects, and smooth gradients are rendered clearly without color degradation.
* **Asynchronous Multi-threaded Processing (Web Workers):** GIF encoding runs in a background multi-threaded environment rather than the main UI thread. Even with a large number of frames, the browser will not freeze, and real-time progress (%) is displayed.
* **Optimization of Compression Ratio:** Complies with standard specifications for LZW dictionary build optimization, drastically reducing the final GIF file size compared to previous versions.

### ✨ Key Features
* **Layer System:** Supports 5 independent layers (`L1` to `L5`) with individual selection and control.
* **Multi-Brush Presets:** Velocity-sensitive pressure simulation for Pen, Sketch Pencil, and Particle-spraying Airbrush.
* **Onion Skinning:** Intelligent lightbox mode visualizing previous/next frames with dynamic opacity and color-coding (Red/Green).
* **Real-time Mini Player:** Seamless loop preview of the ongoing animation via a dedicated top-right floating window.
* **Professional Export Options:** High-quality GIF download powered by `gifshot`, frame-by-frame PNG sequence download, and composite Sprite Sheet generation for game engines.

### 💻 How to Run
1. Save the source code as an `index.html` file.
2. Open the file in any modern web browser (Chrome, Edge, Safari, etc.).
3. Draw using the left toolbar and top palette, then extend the timeline using the `➕ Add Frame` button.
4. Once completed, click the `🎬 Export High-Q GIF` menu in the upper-left corner to download your animation.

---

## 🇯🇵 日本語 (Japanese)

### 🚀 主な改善事項 (Changelog v3.0)
従来の純粋なJavaScript（Vanilla JS）ベースのエンジンから**外部の専門ライブラリ体制**へ全面的に移行したことで、以下のような致命的な限界を克服しました。
* **高品質な色補正（256色量子化）:** 従来の16色制限を解除し、256色のパレット抽出とディザリングをサポート。パステルカラー、エアブラシ効果、微細なグラデーションが劣化することなく鮮明に出力されます。
* **非同期マルチスレッド演算（Web Workers）:** GIFのエンコード処理がメインUIスレッドではなくバックグラウンドのマルチスレッドで実行されるため、フレーム数が多くてもブラウザがフリーズせず、リアルタイムの進行状況（%）が表示されます。
* **圧縮率の最適化:** LZW辞書（Dictionary）ビルド最適化の標準規格に準拠し、最終的なGIFファイルの容量が従来に比べて数倍以上大幅に削減されます。

### ✨ 主な機能
* **レイヤーシステム:** 計5つの独立したレイヤー（`L1`〜`L5`）をサポートし、個別に選択・制御可能。
* **マルチブラシプリセット:** 速度感応型の筆圧擬似表現に対応したペン（Pen）、スケッチ用鉛筆（Sketch）、粒子噴射式エアブラシ（Airbrush）。
* **オニオンスキン（Onion Skin）:** 前後のフレームを不透明度およびカラーガイド（赤/緑）で可視化するインテリジェントなライトボックスモード。
* **リアルタイムミニプレイヤー:** 編集中のアニメーションを右上の専用ウィンドウで無限ループとして常時プレビュー。
* **プロフェッショナルエクスポート:** `gifshot`連動による高品質GIFダウンロード、フレーム別PNGシーケンス書き出し、ゲームエンジン用複合スプライトシート（Sprite Sheet）生成。

### 💻 実行方法
1. ソースコードを `index.html` というファイル名で保存します。
2. ブラウザ（Chrome、Edge、Safariなど）で該当ファイルを開きます。
3. 左側のツールバーと上部のパレットを使って描画し、下部の `➕ Add Frame` ボタンでタイムラインを拡張します。
4. 作業が完了したら、左上の `🎬 Export High-Q GIF` メニューをクリックしてダウンロードします。

---

## 🇨🇳 简体中文 (Simplified Chinese)

### 🚀 主要改进 (Changelog v3.0)
通过从传统的纯 JavaScript（Vanilla JS）引擎全面转型为**外部专业库架构**，成功解决了以下致命瓶颈：
* **高质量颜色校正（256色量化）:** 解除了原有的16色限制，支持256色调色板提取与抖动技术，使蜡笔色调、喷枪效果和细腻的渐变色能够完美呈现而不失真。
* **异步多线程运算（Web Workers）:** GIF 编码在后台多线程中运行，而不是占用主 UI 线程。即使帧数极多，浏览器也不会出现卡死或无响应的情况，并能实时显示编码进度（%）。
* **压缩率优化:** 严格遵守 LZW 字典构建优化的标准规范，使最终导出的 GIF 文件体积较以往版本大幅减少数倍。

### ✨ 核心功能
* **图层系统:** 支持5个完全独立的图层（`L1` 至 `L5`），可分别进行选择与编辑。
* **多款画笔预设:** 支持速度感应仿压感的签字笔（Pen）、素描铅笔（Sketch）以及粒子喷射式喷枪（Airbrush）。
* **洋葱皮功能（Onion Skin）:** 智能灯箱模式，通过调整透明度和色彩向导（红/绿）将前后帧可视化。
* **实时微型播放器:** 在右上角的独立悬浮窗口中，无缝循环预览当前正在编辑的动画。
* **专业级导出支持:** 联动 `gifshot` 导出高质量 GIF、逐帧导出 PNG 序列、以及为游戏引擎生成复合精灵图（Sprite Sheet）。

### 💻 运行方法
1. 将源代码保存为 `index.html` 文件。
2. 使用现代浏览器（Chrome、Edge、Safari 等）双击打开该文件。
3. 利用左侧工具栏和上方调色板进行绘画，点击下方的 `➕ Add Frame` 按钮来增加动画帧。
4. 创作完成后，点击左上角的 `🎬 Export High-Q GIF` 菜单即可下载高质量 GIF 动画。

---

## 🇵🇭 Tagalog / Filipino (필리핀어)

### 🚀 Mga Pangunahing Pagpapabuti (Changelog v3.0)
Sa pamamagitan ng paglipat mula sa lumang purong JavaScript (Vanilla JS) engine patungo sa isang **external specialized library architecture**, nalutas ang mga sumusunod na kritikal na limitasyon:
* **Mataas na Kalidad ng Kulay (256 Color Quantization):** Tinanggal na ang lumang limitasyon na 16 na kulay lamang. Sinusuportahan na ngayon nito ang 256-color palette extraction at dithering, upang ang mga pastel na kulay, airbrush effects, at makinis na gradients ay maipakita nang malinaw nang walang pagkasira ng kulay.
* **Asynchronous Multi-threaded Processing (Web Workers):** Ang GIF encoding ay tumatakbo sa background multi-threaded environment sa halip na sa main UI thread. Kahit marami ang frames, hindi mag-ha-hang o magla-lag ang browser, at ipinapakita ang real-time progress (%).
* **Optimisasyon ng Compression Ratio:** Sumusunod sa standard na mga detalye para sa LZW dictionary build optimization, na nagpapababa sa laki (file size) ng huling GIF file nang ilang beses kumpara sa mga nakaraang bersyon.

### ✨ Mga Pangunahing Tampok (Features)
* **Layer System:** Sinusuportahan ang 5 independiyenteng mga layer (`L1` hanggang `L5`) na may indibidwal na pagpili at kontrol.
* **Multi-Brush Presets:** Simulation ng pressure batay sa bilis para sa Pen, Sketch Pencil, at Particle-spraying Airbrush.
* **Onion Skinning:** Matalinong lightbox mode na nagpapakita ng mga nakaraan at susunod na frame gamit ang dynamic opacity at color-coding (Pula/Berde).
* **Real-time Mini Player:** Walang katapusang loop preview ng ginagawang animasyon sa pamamagitan ng isang hiwalay na floating window sa kanang itaas.
* **Propesyonal na Pag-export (Export):** Pag-download ng mataas na kalidad na GIF gamit ang `gifshot`, pag-download ng frame-by-frame PNG sequence, at pagbuo ng composite Sprite Sheet para sa mga game engine.

### 💻 Paano Patakbuh인 (How to Run)
1. I-save ang source code bilang isang `index.html` file.
2. Buksan ang file sa anumang modernong web browser (Chrome, Edge, Safari, atbp.).
3. Gumuhit gamit ang toolbar sa kaliwa at palette sa itaas, pagkatapos ay palawigin ang timeline gamit ang button na `➕ Add Frame`.
4. Kapag tapos na, i-click ang menu na `🎬 Export High-Q GIF` sa kaliwang itaas na sulok upang i-download ang iyong animasyon.

---

## 📦 Dependencies & License
```html
<script src="[https://cdnjs.cloudflare.com/ajax/libs/gifshot/0.3.2/gifshot.min.js](https://cdnjs.cloudflare.com/ajax/libs/gifshot/0.3.2/gifshot.min.js)"></script>
