## 使用方法
1. calsht.hppをインクルードする.
2. Calshtクラスをインスタンス化する.
3. 手牌を表す長さ34のint型配列を用意する.<br>
n番目の要素がn番目の牌の枚数を格納する(n=0:1m, ..., n=8:9m, n=9:1p, ..., n=17:9p, n=18:1s, .. , n=26:9s, n=27:東, ...,n=30:北, n=31:白, n=32:発, n=33:中).
3. Calshtクラスのメソッドを呼び, シャンテン数を計算する.<br>
各メソッドはシャンテン数+1の値を返す.

  - n面子一雀頭形のシャンテン数を求めるには
    - int calc_lh(int* [手牌を表す配列], int [手牌の枚数])
  - 七対子のシャンテン数も求めるには
    - int calc_sp(int* [手牌を表す配列])
  - 国士無双のシャンテン数を求めるには
    - int calc_to(int* [手牌を表す配列])
  - 一般形のシャンテン数(上記のシャンテン数の最小値)を求めるには
    - int operator()(int* [手牌を表配列], int [手牌の枚数]])

## サンプルプログラム
手牌をランダムに生成し, シャンテン数ごとの出現率とシャンテン数の期待値を計算する。以下のコマンドを実行する。

1. $ make sample.out
2. $ ./sample.out [手牌の枚数] [何通りの手牌を生成するか]<br>
(例)$ ./sample.out 13 100000000

## 注意事項
- C++11以上に対応したコンパイラが必要。
