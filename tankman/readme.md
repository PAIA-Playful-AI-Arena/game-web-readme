## 基本玩法

2~6 位玩家進行團隊對抗賽，GreenTeam 為綠色坦克車，BlueTeam 為藍色坦克車，每隊最多 3 人。透過回傳遊戲指令，操控玩家與射擊砲彈，場上會有各類補給站，可以移動坦克車經過補給站獲取資源。

`遊戲目標` &nbsp;&nbsp;&nbsp; 時間內殲滅敵對，或高分隊伍獲勝。
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 分數計算方式：
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 敵方失去的生命次數 _ `20` 分。
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 每擊中一次牆壁 _ `1` 分。
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 擊破牆壁 \* `5` 分。

`失敗條件`&nbsp;&nbsp;&nbsp; 生命歸零，或遊戲時間結束時分數較敵隊低。

## 遊戲系統

#### 坦克車

- 前進、後退速度（8 px）
- 車身轉彎角度（45 度）
- 砲管旋轉角度（45 度）
- 生命機會（3 次）
- 燃油（100）
- 彈匣（10）

#### 牆

- 生命次數（3）
- 透明設定（依照生命次數決定）

#### 補給站 - 燃油

- 玩家經過補充 30 點燃油，超過 100，則無效。
- 與玩家或子彈碰撞後消失，30 幀後隨機位置顯示。

#### 補給站 - 彈藥

- 玩家經過補充 5 顆彈藥，超過 10，則無效。
- 與玩家或子彈碰撞後消失，30 幀後隨機位置顯示。

#### 鍵盤控制

![top](https://hackmd.io/_uploads/HyxmgXWk0.png)&nbsp;&nbsp;&nbsp;![bottom](https://hackmd.io/_uploads/B1o7xQZJC.png)&nbsp;&nbsp;&nbsp;![left-key](https://hackmd.io/_uploads/SyXNeX-JR.png)&nbsp;&nbsp;&nbsp;![right-key](https://hackmd.io/_uploads/Sko4gXZk0.png)&nbsp;&nbsp;&nbsp;1P 的移動和轉彎控制

![z-key](https://hackmd.io/_uploads/HkOrx7-yA.png)&nbsp;&nbsp;&nbsp;![x-key](https://hackmd.io/_uploads/rJx8gXW1C.png)&nbsp;&nbsp;&nbsp;1P 砲管的左/右旋轉控制

![m-key](https://hackmd.io/_uploads/SJSOembkC.png)&nbsp;&nbsp;&nbsp;1P 的射擊鍵

![w-key](https://hackmd.io/_uploads/r1GKgQ-kA.png)&nbsp;&nbsp;&nbsp;![s-key](https://hackmd.io/_uploads/HJcYemWkA.png)&nbsp;&nbsp;&nbsp;![A-key](https://hackmd.io/_uploads/Bk-9l7b1A.png)&nbsp;&nbsp;&nbsp;![D-key](https://hackmd.io/_uploads/SJwqxmWJA.png)&nbsp;&nbsp;&nbsp;2P 的移動和轉彎控制

![q-key](https://hackmd.io/_uploads/SJEseXWyA.png)&nbsp;&nbsp;&nbsp;![e-key](https://hackmd.io/_uploads/BJYigmZJR.png)&nbsp;&nbsp;&nbsp;2P 砲管的左/右旋轉控制

![f-key](https://hackmd.io/_uploads/B1E2lQ-yR.png)&nbsp;&nbsp;&nbsp;2P 的射擊鍵

![i-key](https://hackmd.io/_uploads/BJJalQZk0.png)&nbsp;&nbsp;&nbsp;![j-key](https://hackmd.io/_uploads/HkE6eQbyC.png)&nbsp;&nbsp;&nbsp;![k-key](https://hackmd.io/_uploads/rki6gQWyR.png)&nbsp;&nbsp;&nbsp;![l-key](https://hackmd.io/_uploads/SkM0lX-JA.png)&nbsp;&nbsp;&nbsp;上下左右移動遊戲畫面

![o-key](https://hackmd.io/_uploads/B1E1Zm-kC.png)&nbsp;&nbsp;&nbsp;![u-key](https://hackmd.io/_uploads/SkhAxXZyC.png)&nbsp;&nbsp;&nbsp;放大/縮小遊戲畫面

![h-key](https://hackmd.io/_uploads/HkwlWmZyC.png)&nbsp;&nbsp;&nbsp;可隱藏畫面中的遊戲資訊。

![p-key](https://hackmd.io/_uploads/B1W-ZQ-JA.png)&nbsp;&nbsp;&nbsp;可暫停遊戲。（mlgame 10.2 後版本才有效）

#### 座標系統

- 單位為 px。
- 螢幕大小 1000 x 600。
- 單元格 25 x 25，可放置一個物件。
