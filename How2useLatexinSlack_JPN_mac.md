環境：macOS High Sierra 10.13.6
Slack Version 4.4.2


返信先: ツイッター
@aokikenichiさんが
「SlackでTeX書けますね。」
と投稿しており、
結城浩
@hyuki 2018年5月22日
これを使っています。

https://github.com/fsavje/math-with-slack
が紹介してあった。

一方、
Mac and Linux
Run the following in a terminal:

curl -OL https://github.com/fsavje/math-with-slack/releases/download/v0.2.5/math-with-slack.sh
sudo bash math-with-slack.sh
を実行しても動かないので、よく記事を読んで見るとSlack 4 では動作不良があるとのこと。

⚠️ ⚠️ Slack 4 introduces a content security policy to prevent code injections. This breaks the math-with-slack script. A solution is in the making. ⚠️ ⚠️

https://github.com/fsavje/math-with-slack/issues/51

src/static/は確かに存在せず、src/distになっている。math-with-slack.shをその中に入れて見るなどして、slack再起動したがやはりMathJaxは動かない（tex を含むslackメッセージの数式はコンパイルされない）

ディスカッションでは、thisiscam氏の

https://github.com/thisiscam/math-with-slack/tree/v3


が良いとのこと。

最終的にこのコードで動作した。
https://github.com/thisiscam/math-with-slack/tree/v3
の
Mac and Linux

Run the following in a terminal:

curl -OL https://raw.githubusercontent.com/psg-mit/math-with-slack/v3/math-with-slack.py
sudo python math-with-slack.py


https://github.com/thisiscam/math-with-slack/tree/v3


---

In the plotting of a mathematical function, like $\sin(x)$, a description with $\pi$ frequently appears. In the MATLAB, if you want to set a period $[-2\pi,2\pi]$ you set “time=[-2*pi,2*pi]” for example. Similarly, a summation like $$ S=\sum_{i=1}^{N}{a^2}$$ can be calculated by the following code.
N=10; S=0; a=2;
for i=1:N
S=S+a.^2;
end
disp(S);
Then you can translate some mathematical description to computer language description.
---
このような記述が、MathJaxでコンパイルされる（注：$ $ はインライン表示、$$ $$ は改行表示）。

https://github.com/fsavje/math-with-slack/issues/51

<img src="https://latex.codecogs.com/gif.latex?\inline&space;x[k]\&space;(k=1&space;\dots&space;N)" />
