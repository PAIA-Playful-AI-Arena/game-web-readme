# 基本玩法

<br />

在遊戲時間截止前到達迷宮的終點，並且盡可能減少碰撞牆壁的次數。目前提供 6 種迷宮地圖，迷宮編號從 1 開始，預設為 1 號地圖。

<br />

`遊戲目標`&nbsp;&nbsp;&nbsp; 在遊戲時間截止前到達迷宮的終點，並且盡可能減少碰撞牆壁的次數。

`排名條件`&nbsp;&nbsp;&nbsp; 幽浮所走的距離：經過的檢查點愈多則排名愈前。幽浮與牆壁碰撞次數：若兩台走經的檢查點數量相同，則碰撞次數少者排名愈前。幽浮前進速度：若前兩項評分依據皆平手，則比較走到最末檢查點時的遊戲時間，愈早走到者排名愈前。

<br />

# 遊戲系統

<br />

## 幽浮

- 控制左右輪轉速，達到前進、後退、轉彎的目的。 左輪與右輪的轉速由玩家程式控制，範圍為 -255 ~ 255。 速度為 0 時相當於停在原地，速度為負值實則輪子向後轉，速度為正時輪子向前轉。
- 可以選擇 4 或 6 個感測器數量，預設為 6。

## 感測器

- 感測器測量距離的起點為自走車車身外圍，終點為該感測方向上最靠近的牆壁。 感測器的數量可以選擇 3 或 5 個。區別在於是否有左、右前方的感測器。

## 鍵盤控制

<br />

![top](/assets/icons/top.svg)&nbsp;&nbsp;&nbsp;![w-key](/assets/icons/w.svg)&nbsp;&nbsp;&nbsp;左右輪輸出 -255 ~ 255，由玩家程式控制。

![bottom](/assets/icons/bottom.svg)&nbsp;&nbsp;&nbsp;![s-key](/assets/icons/s.svg)&nbsp;&nbsp;&nbsp;??

![left-key](/assets/icons/left.svg)&nbsp;&nbsp;&nbsp;![A-key](/assets/icons/a.svg)&nbsp;&nbsp;&nbsp;??

![right-key](/assets/icons/right.svg)&nbsp;&nbsp;&nbsp;![D-key](/assets/icons/d.svg)&nbsp;&nbsp;&nbsp;??

<br />

## 座標系統

- 使用 Box2D 的座標系統，單位為 `cm`，每公分換算為 `4` 像素。
- `左下角`為原點 (0,0)，Ｘ軸向右為正，Y 軸向上為正。
- 所有座標皆回傳物件`左上角`之座標。 幽浮 10 x 10 cm。
- 檢查點 ?? x ?? cm。
- 終點 15 x 15 cm。
