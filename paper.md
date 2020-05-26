Since 2020-05-16

<details><summary>機械学習を用いた Wi-Fi と BLE の統合フィンガープリントによる マルチユーザ屋内位置推定に関する一検討</summary><div>

## まえがき
- 屋外→GNSS，LOS環境
- 屋内→NonLOS環境で位置推定精度が低下する
- RSSIから距離を一意に推定するのは難しい
→フィンガープリント（予めRSSIの測定データを得ておき，推定時に照合して最尤推定）が有効
→しかし，物体の位置関係が静的でもRSSIが一定値を取るとは限らず，チャネルの状態に応じて変動する
→そこで，WifiとBLEのRSSI両方使って機械学習

## 2.1 RSSIを用いた位置推定
- 3点測位が有名だが，環境の変化に弱い（自由空間伝搬に基づくから）

## 2.2 フィンガープリントを用いた位置推定
- ３点測位より精度が高いが，それでもRSSIの確率的変動は考慮する必要がある．
- WifiかBLEどちらかのみの研究が多いので，どっちも使えばデータ量が多くなって精度向上が期待できる？

## 3.1 多クラス分類モデル
## 3.2 多層パーセプトロン
## 3.3 学習の効率化
## 4. 特性評価
- 送信機をシングルの場合，マルチ（４台）の場合で実験．受信機は８台．推定候補点18
- 受信周期はWifi：6秒，BLE：0.3秒
- RSSIは0-10秒の平均，1-11秒の平均といった風にして訓練データとする
- 訓練データの正解位置は，受信機搭載のカメラで写真を撮っておき，それとRSSI取得時刻からラベリング（無理やりやな・・）
- ２４時間分の訓練データで学習し，１時間分のテストデータで推定
</divs></details>

<details><summary>強化学習を用いた QoE ドリブンな適応型ビデオストリーミングの性能改善</summary><div>

## はじめに
- 今後ビデオトラフィックの占める割合は増えていく．
→輻輳が多くなる→QoS，QoEが低下
→強化学習でAdaptiveStreaming（MPEG-DASH配信）

## 2.1 MPEG-DASH
## 2.2 QoEモデル
- 他論文で提案されているQoEモデルから，MOSを推定する

## 2.3 ABR（Adaptive Bitrate）
- 様々なアルゴリズムがある（Rate-based，Buffer-basedなど）

## 2.4 Pensieve
- 深層強化学習を使用したABRアルゴリズム，及びそれを実装した配信方法

## 3 山岸のモデルを元に強化学習を行った適応レート制御手法
- Pensieveで定義されているQoEメトリックを，山岸のモデルを元に改良

## 4.1 実験環境と評価項目
- Buffer-based，MPCと比較

## 4.2 評価シナリオ
- ３種類のスループットトレースに従って実験

## 5 評価結果
</divs></details>

<details><summary>高効率無線LANにおけるCCA閾値制御と送信電力制御の容量改善効果</summary><div>


</divs></details>

<details><summary>Wi-Fi の送信を考慮した CCA 時間制御による LTE-LAA のリソース制御</summary><div>

- 時間制御はあまり提案されてない
- 複数回送信ごとにCCA時間を更新
- LTE周波数帯不足→アンライセンスバンド（５GHz）と束ねるCA（Carrier Aggregation）→Wifiと共存するためにLBT（Listen Before Talk）
- 無線LANのQoSであるEDCA（Enhanced Distributed Enhanced Distributed Channel Access）
  - AC（Access Category）ごとにキューを持ち，それぞれでCSMA/CAを行う
  - EDCAではDIFSではなくAIFSがACごとに設定されている
  - 一度送信権を獲得したACはその後SIFS間隔で連続して送信できる
  - 連続送信可能な時間はTxOPlimitに設定されている
- キャリアセンスは使用する周波数帯を調べるもの
</divs></details>

<details><summary>ProCCA: Protective Clear Channel Assessment in IEEE 802.11 WLANs</summary><div>

## Abstract
- 物理層の情報も使ったCCAメカニズム（IEEE 802.11ac）

## Introduction
- Spatial Reuseは重要であるなぜならSharedメディアにおいて同時送信を可能にすることでネットワーク容量を向上させるため．（特に高密度環境では）
- CST（Carrier Sense Threshold）
- 先行研究の一つでは隠れ端末にフォーカスして保守的な結果になった．
- 一方で，FERをもとにしたヒューリスティックなアプローチもあった．これは↑のよりは保守的でない．
- 現状のCCAはRSS（RSSI）のみで判断している．

## Background and Motivation
- 他の基地局の電波をキャプチャーしてしまう可能性はSIR（Signal to Interference Ratio）によってわかる
- フレームを先頭からセンスするわけだが，RSSがCSTを超えるとチャネルはビジーと判断される．
- CSTを低くすると晒し端末問題が起き，高くすると隠れ端末問題が起きる．
- 物理層ヘッダの予約ビットをsource ID, destination ID, and signal qualityに使った

## Protective CCA
- ヘッダ情報からSignal Quality Tableを作成
- チャネルの非対称性も考慮する必要がある

## Performance Evaluation
## Concluding Remarks
</divs></details>

<details><summary>Hybrid Scheduling in Heterogeneous Half-and Full-Duplex Wireless Networks</summary><div>

H-GMS（Hybrid-GMS，GMSとQ-CSMAを組み合わせたもの）という分散スケジューリングアルゴリズムを提案．半二重と全二重の混ざったヘテロジニアスネットワークにおいて遅延や公平性，スループットを評価．
- 無線スケジューリングアルゴリズムとして伝統的なアプローチが３つある．
  - MWS（Maximum Weight Scheduling）：各FDユーザとAP間でキュー長情報の共有が必要でオーバヘッド大．
  - GMS（Greedy Maximal Scheduling）：他より遅延が大きい．一般的にスループット最適でない．
  - Q-CSMA（Queue-based）：長い遅延をもたらす過剰なキュー長．

## Model and Preliminaries
### A. Network Model
- AP1＋ユーザNのネットワークを考える．N人のうちNF人が全二重でNHが半二重．
- 有向星グラフG=(V,E)とすると頂点V＝N+1個，辺E＝２N本
### B. Traffic Model, Schedule, and Queues
### C. Capacity Region and Throughput Optimality
</divs></details>
