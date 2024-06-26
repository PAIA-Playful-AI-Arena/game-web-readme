# 基本玩法

<br />

遊戲最多可以四個人同時進行，有三種遊戲模式。

<br />

- **普通模式**：若車子之間發生碰撞，則雙方皆淘汰出局。
- **重生模式**：玩家與其他車子發生碰撞時並不會出局，唯速度減速為 0，並進入三秒的無敵時間，此三秒內與其他車子碰撞不會導致玩家降速。
- **金幣模式**：玩家之間可以控制車子爭奪金幣。

<br />

`遊戲目標`

- **普通模式**：以最快的速度到達終點。
- **金幣模式**：在遊戲時間截止前，盡可能吃到更多的金幣
- **重生模式**：以最快的速度到達終點。

`失敗條件`&nbsp;&nbsp;&nbsp; 車子在遊戲過程中被淘汰，即算失敗。

<br />

# 遊戲系統

<br />

## 玩家車

- 彩色車子。
- 車子的最高速度為 15 px/frame，當車子左右平移時速度將會略微下降為 14.5 px/frame。 車子沒有加速或剎車時，會以 0.9 px/frame 左右的速度怠速前進。
- 前方有車 (不論是電腦還是玩家) 會剎車減速，前方無車則會不斷加速至最高速。

## 電腦車

- 白色車子。
- 電腦的車子從畫面左方或右方出現，不會切換車道。
- 電腦的車子每台車最高速度皆不一樣，範圍為 10~14。
- 前方有車 (不論是電腦還是玩家) 會剎車減速，前方無車則會不斷加速至最高速。

## 金幣

- 金幣隨機從畫面右方出現，以 5 px/frame 的速度移動。
- 電腦車子碰到金幣時金幣不會消失。

## 行動機制

<br />

![top](/assets/icons/top.svg)&nbsp;&nbsp;&nbsp;車子以 3px/frame 的速度向左平移

![bottom](/assets/icons/bottom.svg)&nbsp;&nbsp;&nbsp;車子以 3px/frame 的速度向右平移

![left-key](/assets/icons/left.svg)&nbsp;&nbsp;&nbsp;車子向前加速

![right-key](/assets/icons/right.svg)&nbsp;&nbsp;&nbsp;車子剎車減速

<br />

車子的最高速度為 15px/frame，當車子左右平移時速度將會略微下降為 14.5px/frame。
車子沒有加速或剎車時，會以 0.9px/frame 左右的速度怠速前進。

<br />

## 座標系統

- 使用 pygame 座標系統，左上角為 (0,0)，x 方向以右為正，y 方向以下為正，單位為 px。
- 螢幕大小 1000 x 700。
- 車子大小 60 x 30。
- 金幣大小 30 x 30。
