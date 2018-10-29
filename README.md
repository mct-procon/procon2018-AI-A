# procon2018-AI-A
第29回全国高等専門学校プログラミングコンテスト 競技部門 AI Program. Developerd by 松江高専, Naoto Kawakami, Rikuto Sueta, Renju Aoki, Go Suzuki, and some members.

## Requirements & Develop Environment

> OS : Windows 10 April 2018 Update  
> CPU : Haswell or later Intel CPUs, Ryzen  
> Memory : more than 2GBytes  
  
> Softwares  
> VisualStudio 2017 Update 8 or later  
> .Net Core 2.1 or later  
> C# 7.3 or later  

# 概要
課題のゲームを先手と後手が交互に操作するゲームとみなし，MiniMax法とαβ法を用いて実装したAIプログラムです．以下の改良があります．  
>・評価関数を改良しています．具体的には以下の通りです．  
>　　全ターンの2/3未満の時は，自陣の位置の分散を評価値に含めています．後半に囲み領域を増やす狙いがあります．  
>　　全ターンの2/3未満の時は，囲み領域のスコアを0.8倍しています．これは，囲み領域は壊されやすいためです．  
>・反復深化をしています．これにより，時間のある限りAIが深く読みます．  
>・ノードの深さが奇数の時（交互に打つゲームと考えているので，奇数の場合，片方のプレイヤーしか動かないことになります．），貪欲に動くことで，探索延長しています．  
