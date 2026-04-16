# 遊戲說明

<br />

使用你的 AI 操控 Proly 小精靈，在各式各樣的地形闖關冒險。遊戲目前有兩種模式，『定向越野』模式與『大亂鬥』模式。
<br />

## 定向越野

`遊戲目標` &nbsp;&nbsp;&nbsp;依照順序通過所有旗子，最快通過者獲勝。

## 大亂鬥
`遊戲目標` &nbsp;&nbsp;&nbsp;時間內，存活到最後，血量最高者獲勝。

<br />

# AI 的行動

<br />


- 1P（本機）

    移動方式：![W-key](/assets/icons/w.svg) ![S-key](/assets/icons/s.svg) ![A-key](/assets/icons/a.svg) ![D-key](/assets/icons/d.svg)

    切換道具：![Q-key](/assets/icons/q.svg)

    使用道具：![E-key](/assets/icons/e.svg)

- 2P（本機）

    移動方式：![Up-key](/assets/icons/top.svg) ![Down-key](/assets/icons/bottom.svg) ![Left-key](/assets/icons/left.svg) ![Right-key](/assets/icons/right.svg)

    切換道具：![Shift-key](/assets/icons/shift.svg)

    使用道具：![Ctrl-key](/assets/icons/ctrl.svg) 或 ![Alt-key](/assets/icons/alt.svg)

- 3P（本機）

    移動方式：![Y-key](/assets/icons/y.svg) ![H-key](/assets/icons/h.svg) ![G-key](/assets/icons/g.svg) ![J-key](/assets/icons/j.svg)

    切換道具：![T-key](/assets/icons/t.svg)

    使用道具：![U-key](/assets/icons/u.svg)

- 4P（本機）

    移動方式：![P-key](/assets/icons/p.svg) ![Semicolon-key](/assets/icons/semicolon.svg) ![L-key](/assets/icons/l.svg) ![Apostrophe-key](/assets/icons/apostrophe.svg)

    切換道具：![O-key](/assets/icons/o.svg)

    使用道具：![Bracket-left-key](/assets/icons/bracket_left.svg)

<br />


# 座標系統
點選 `F1` 可以看到座標資訊，系統中會直接提供水平座標與垂直座標，可參考此圖。


# 遊戲物件

<br />

## 地形
遊戲中可以取得不同的地形資訊
- 水，程式編號 `-1`，掉到水中就會死亡重生。
- 陸地，程式編號 `0`，可以安全行走的地方。
- 障礙物，程式編號 `1`，無法直接穿越。



## 泥坑
- 尺寸大小：半徑 1 公尺
- 效果：大幅減慢玩家移動速度

## 旗子
- 需要依照編號蒐集
- 位置依照該地圖所設定位置，隨機產生、隨機排序，因此旗子出現的位置是有限組合。

## 道具

- 治療蛋糕，程式編號 `1`，可以恢復1點生命值。
- 加速咖啡，程式編號 `2`，短時間內提升移動速度。
- 炸彈，程式編號 `3`，丟出去可以造成範圍傷害，中心傷害較高。
- 手裡劍，程式編號 `4`，直線飛行的投射物，可造成3點傷害。
- 護盾，程式編號 `5`，短時間內獲得暫時免傷效果。



<!-- # 自訂關卡

<br />

除了 PAIA 提供的關卡，你也可以嘗試自行設計關卡，讓磚塊出現在不同位置來營造更多遊戲樂趣，請參考[自訂地圖教學]()。 -->

# 適用賽制
- `闖關賽`
- `淘汰賽`
