# 基本玩法

<br />

在茫茫的宇宙中，有許多的障礙物，要如何閃過障礙物，走到白洞前往新世界呢？本遊戲提供多元的關卡，隨著遊戲難度提升，考驗各位玩家如何在多變的環境下，依然能夠走到終點。小心，碰到牆壁可是會爆炸的！！

<br />

`遊戲目標`&nbsp;&nbsp;&nbsp; 在遊戲時間截止前到達迷宮的終點，並且盡可能減少碰撞牆壁的次數。

`排名方式`&nbsp;&nbsp;&nbsp; 分數高者獲勝
    - 分數＝ `檢查點數量`x10000 - `碰撞次數`x10 - `使用時間`x0.001


<br />

# AI 的行動
需同時給予左右兩個輪子移動的力量，力量介於 `-255` 到 `255` 之間，透過控制左右輪轉速，即可達成前進、左轉、右轉、後退等動作。

<br />

![top](/assets/icons/top.svg)&nbsp;&nbsp;&nbsp;![w-key](/assets/icons/w.svg)&nbsp;&nbsp;&nbsp;左右輪輸出 -255 ~ 255，由玩家程式控制。

![bottom](/assets/icons/bottom.svg)&nbsp;&nbsp;&nbsp;![s-key](/assets/icons/s.svg)&nbsp;&nbsp;&nbsp;??

![left-key](/assets/icons/left.svg)&nbsp;&nbsp;&nbsp;![A-key](/assets/icons/a.svg)&nbsp;&nbsp;&nbsp;??

![right-key](/assets/icons/right.svg)&nbsp;&nbsp;&nbsp;![D-key](/assets/icons/d.svg)&nbsp;&nbsp;&nbsp;??

# 座標系統

- 使用 `Box2D` 的座標系統，長度單位為 `cm` 。
- `左下角`為原點 (0,0)，`Ｘ軸`向`右`為正，`Y軸`向`上`為正。
- 使用 Tiled 來繪製地圖，地圖一格為 `5cm`。
- 所有座標皆回傳物件`中心點`之座標。

<br />

## 幽浮

- 大小 10cm x 10cm
- 控制左右輪轉速，達到前進、後退、轉彎的目的。 左輪與右輪的轉速由玩家程式控制，範圍為 -255 ~ 255。 速度為 0 時相當於停在原地，速度為負值實則輪子向後轉，速度為正時輪子向前轉。


## 感測器

- 可透過感測器測量距離`車身`到`牆壁`的距離。
- 一台車有 6 個感測器。

## 檢查點
- 為一個線段，通過此線段，檢查點數量加1
  
## 終點
- 大小 15cm x 15cm 
- 為一個白色蟲洞，象徵逃出迷宮，可以前往新世界。

<br />


# 關卡設計

<br />

除了 PAIA 提供的關卡，你也可以嘗試自行設計地圖關卡，甚至可以透過[自訂競賽](https://)邀請朋友一起來挑戰喔！

<br />

[地圖編輯器](https://github.com/PAIA-Playful-AI-Arena/Maze_Car/blob/main/map_editor.md)


<br />


# 適用賽制
- `闖關賽`
- `積分賽`