# 遊戲說明

<br />
在錯綜復雜的棋盤迷宮中，想辦法讓你的AI自走車突破重圍，不會迷失在其之中，走到終點。本遊戲也提供多元的關卡，隨著遊戲難度提升，考驗各位玩家如何在多變的環境下，依然能夠逃出迷宮。

<br />

`遊戲目標`&nbsp;&nbsp;&nbsp; 在時間結束前，抵達終點。

`失敗條件`&nbsp;&nbsp;&nbsp; 時間結束前，自走車尚未走到終點，即算失敗。

<br />

# AI 的行動

需同時給予左右兩個輪子移動的力量，力量介於 `-255` 到 `255` 之間，透過控制左右輪轉速，即可達成前進、左轉、右轉、後退等動作。

<br />

![top](/assets/icons/top.svg)&nbsp;&nbsp;&nbsp;![w-key](/assets/icons/w.svg)&nbsp;&nbsp;&nbsp;左右輪固定輸出 100。

![bottom](/assets/icons/bottom.svg)&nbsp;&nbsp;&nbsp;![s-key](/assets/icons/s.svg)&nbsp;&nbsp;&nbsp;左右輪固定輸出 -100。

![left-key](/assets/icons/left.svg)&nbsp;&nbsp;&nbsp;![A-key](/assets/icons/a.svg)&nbsp;&nbsp;&nbsp;左輪輸出增加 100。

![right-key](/assets/icons/right.svg)&nbsp;&nbsp;&nbsp;![D-key](/assets/icons/d.svg)&nbsp;&nbsp;&nbsp;右輪輸出增加 100。

- 上、下、左、右為 1P，Ｗ、Ａ、Ｓ、Ｄ為 2P。

<br />

# 座標系統

- 使用 `Box2D` 的座標系統，長度單位為 `cm` 。
- `左上角`為原點 (0,0)，`Ｘ軸`向`右`為正，`Y軸`向`上`為正。
- 使用 Tiled 來繪製地圖，地圖一格為 `5cm`。
- 所有座標皆回傳物件`中心點`之座標。
- 每 `1cm` 換算為 `3.2px` 。

# 遊戲物件

<br />

## 自走車

- 彩色長方形搭配輪子和感測器的小車，每台車的顏色不同。
- 自走車 12.5 x 10 cm。
- 提供的座標為中心點的座標。

## 感測器

- 可透過感測器測量距離`車身`到`牆壁`的距離。
- 一台車有 5 個感測器。

## 迷宮地圖

- 迷宮的白色區塊為實牆，自走車需繞道尋找出口。

## 檢查點

- 綠色牌子
- 每通過一個檢查點，系統皆會紀錄時間，在沒有通過終點情況下，就是判斷誰最快通過最多檢查點。
- 檢查點大小 15 x 15 cm。

## 終點

- 紅色牌子，整個迷宮的終點。
- 愈快碰到分數愈高。
- 終點大小 15 x 15 cm。

# 計分機制

1. 每通過一個檢查點、終點得 `1000分`
2. 每多花`一個frame`走到檢查點、終點，扣`1分`
3. `總分 = 檢查點個數x1000 - 花費時間`

# 關卡設計

<br />

除了 PAIA 提供的關卡，你也可以嘗試自行設計地圖關卡，甚至可以透過[自訂競賽](https://app.paia-arena.com/zh/user/my-competition)邀請朋友一起來挑戰喔！

<br />

[地圖編輯器](https://github.com/PAIA-Playful-AI-Arena/Maze_Car/blob/main/map_editor.md)

<br />

# 適用賽制

- `闖關賽`
- `積分賽`
