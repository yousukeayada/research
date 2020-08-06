---
marp: true
theme: cs29fine
pagination: true
---

# Joint Channel Selection and Spatial Reuse for Starvation Mitigation in IEEE 802.11ax WLANs

---

## Abstract
- 我々の主な目的は、飢餓を緩和しながらスループットを向上させることである。
- 我々は非協力的なゲームを定式化し、それが正確なポテンシャルゲーム（EPG：Exact Potential Game）であることを証明した。
- 提案したゲームモデルに基づいて、局所的な情報交換のみを用いた共同チャネル選択および空間再利用アルゴリズムを設計する。

---

## 関連研究（イントロより抜粋）
- ６，７：送信電力にフォーカス
- ８：CCA閾値にフォーカス
  - これらのほとんどは飢餓問題を考慮していない
- ９，４：本論文と密接に関係。各APの送信電力とCCA閾値の積を共通定数とすることで、asymmetric link starvationを完全に解消する
- ５：chainトポロジーの数を減らすことで、FIM starvationを緩和するチャネル選択スキームを提案
- １０：提案ゲームがEPGであることが証明される

---

## 目次
1. INTRODUCTION
1. SYSTEM MODEL
1. FORMULATION OF POTENTIAL GAMES
1. PROPOSED JOINT CHANNEL SELECTION AND SPATIAL REUSE ALGORITHM
1. SIMULATION
1. CONCLUSION

---

## INTRODUCTION
- 無線LANが急激に増えているhttps://wigle.net/
- 高品質の音声・ビデオ要求も増えている
- ax では空間再利用の向上にフォーカスしていて、例えば、送信電力を下げるか、CCA閾値を上げる
- しかし不適切な調整をすると、飢餓問題が起きる。本論文では２タイプの問題にフォーカスする
  - asymmetric link starvation：片方は気付いてるがもう片方は気付いていない。気付いていない方が送信し続けてしまう
  - flow-in-the-middle（FIM）starvation：二台の送信機に挟まれた送信機。両端は互いに気付いていないが、真ん中の挟まれた送信機はどちらにも気づく

---

## INTRODUCTION
- utility function （効用関数）
  - 最初の2つの効用関数は、各プレイヤーの戦略をチャネルとCCA閾値の組み合わせに拡張した2つの先行研究のものを拡張したもの
  - 最後の効用関数は、提案された効用関数であり、最初の2つの効用関数の加重和

---

## SYSTEM MODEL

---

## FORMULATION OF POTENTIAL GAMES

---

## PROPOSED JOINT CHANNEL SELECTION AND SPATIAL REUSE ALGORITHM

---

## SIMULATION

---

## CONCLUSION
- 本論文では、密なIEEE 802.11ネットワークにおけるスターベーション問題に対処するためのチャネルと電力の共同制御問題を提案する。
- 我々は非協力的なゲーム理論的フレームワークを提案し、このフレームワークに基づいて[* 分散アルゴリズム]を設計し、[* スループットの向上と飢餓の軽減を同時に実現]する
- 提案されたゲームモデルはEPGであり、提案されたアルゴリズムが収束することが保証されていることを示す
- より望ましいNEへの収束を保証する最初の2つの効用関数のいくつかの他の組み合わせが、今後の研究で検討される