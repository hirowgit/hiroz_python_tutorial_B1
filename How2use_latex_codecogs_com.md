http://idken.net/posts/2017-02-28-math_github/  
https://latex.codecogs.com  
https://www.codecogs.com/latex/eqneditor.php  
  
受光した信号を
<img src="https://latex.codecogs.com/gif.latex?\inline&space;x[k]\&space;(k=1&space;\dots&space;N)" />
、サンプリング周波数を
<img src="https://latex.codecogs.com/gif.latex?\inline&space;F_s" />
とします。  
ここでは
<img src="https://latex.codecogs.com/gif.latex?\inline&space;x[n]" />
から周波数
<img src="https://latex.codecogs.com/gif.latex?\inline&space;F_s&space;\frac{n}{N}\&space;(n&space;\in&space;\mathbb{N})" />
成分の強度を計算するとします。  

まず

<img src="https://latex.codecogs.com/gif.latex?X[n]&space;=&space;\sum_{k=0}^{N-1}x[k]\exp({-j\frac{2&space;\pi&space;nk}{N}})"/>

を計算します。  

次に
<img src="https://latex.codecogs.com/gif.latex?\inline&space;X[n]&space;\in&space;\mathbb{C}" />
の絶対値を計算することで  
<img src="https://latex.codecogs.com/gif.latex?\inline&space;x[k]" />
に含まれる周波数
<img src="https://latex.codecogs.com/gif.latex?\inline&space;F_s\frac{n}{N}" />
の振幅を得ることができます。
