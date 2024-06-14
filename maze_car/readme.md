# 基本玩法

<br />

遊戲最多可以六個人同時進行，有三種遊戲模式。

<br />

- **經典迷宮**：純靜態迷宮，多種地圖可選。
- **移動迷宮**：有移動牆的動態迷宮，多種地圖可選。

<br />

`遊戲目標`&nbsp;&nbsp;&nbsp; 純靜態迷宮，多種地圖可選。

`失敗條件`&nbsp;&nbsp;&nbsp; 時間結束前，自走車尚未走到終點，即算失敗。

<br />

# 遊戲系統

<br />

## 自走車

- 彩色長方形搭配輪子和感測器的小車，每台車的顏色不同。

## 感測器

- 感測器測量距離的起點為自走車車身外圍，終點為該感測方向上最靠近的牆壁。
- 感測器的數量可以選擇 3 或 5 個。區別在於是否有左、右前方的感測器。 迷宮地圖 迷宮的白色區塊為實牆，自走車需繞道尋找出口。

## 迷宮地圖

- 迷宮的白色區塊為實牆，自走車需繞道尋找出口。

## 鍵盤控制

<br />

![top](/assets/icons/top.svg)&nbsp;&nbsp;&nbsp;![w-key](/assets/icons/w.svg)&nbsp;&nbsp;&nbsp;左右輪固定輸出 100。

![bottom](/assets/icons/bottom.svg)&nbsp;&nbsp;&nbsp;![s-key](/assets/icons/s.svg)&nbsp;&nbsp;&nbsp;左右輪固定輸出 -100。

![left-key](/assets/icons/left.svg)&nbsp;&nbsp;&nbsp;![A-key](/assets/icons/a.svg)&nbsp;&nbsp;&nbsp;左輪輸出增加 100。

![right-key](/assets/icons/right.svg)&nbsp;&nbsp;&nbsp;![D-key](/assets/icons/d.svg)&nbsp;&nbsp;&nbsp;右輪輸出增加 100。

- 上、下、左、右為 1P，Ｗ、Ａ、Ｓ、Ｄ為 2P。
- 透過控制左右輪轉速，達到前進、後退、轉彎的目的。

## 座標系統

- 使用 Box2D 的座標系統，單位為 `cm`，每公分換算為 `4` 像素。
- `左上角`為原點 (0,0)，Ｘ軸向右為正，Y 軸向上為正。
- 所有座標皆回傳物件`左上角`之座標。
- 自走車 12.5 x 10 cm。
- 檢查點 15 x 15 cm。
- 終點 15 x 15 cm。
