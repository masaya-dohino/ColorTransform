## 色変換
シミュレーション値の色変換プログラム

2次元NS-FDTDにより遠方界変換まで行われた値（散乱強度）を角度に対する色情報として出力

## 手法
色変換は可視光線の波長ごとの各反射率から、RGB値を求める変換である。色変換を行うには、反射率をXYZ系へ写像し、それからRGB値に変換するという方法を用いる。XYZ等色関数とは、CIEが提唱した波長スペクトルとXYZ刺激値との対応関数である。実際に3刺激値XYZ値は以下の式で求める。

![image](https://user-images.githubusercontent.com/57475794/99529373-0a2d7b80-29e3-11eb-81c2-99dee9f926f4.png)


ここで、λは波長を表し、x ̂(λ),y ̂(λ),z ̂(λ)はλに対するx,y,z等色関数の値を、S(λ), R(λ)は標準の光の分布と反射率を表す。kはYの値が測光量に一致するように定めるための比例定数である。ここで、光の分光分布とは、JIS Z8720で規定された太陽光に分布を表すStandard Illuminant 65(D65)を用いる。
　また、XYZ刺激値からRGB値への変換は以下の式で与えられる。

![image](https://user-images.githubusercontent.com/57475794/99529417-203b3c00-29e3-11eb-89d8-7ec2c6876d75.png)




## シミュレーションの変換結果
定義された髪の毛の散乱体モデル


![image](https://user-images.githubusercontent.com/57475794/99529538-51b40780-29e3-11eb-8740-d70d31fd760b.png)

出力された角度に対する色情報

![image](https://user-images.githubusercontent.com/57475794/99529653-7e681f00-29e3-11eb-9a97-1b949701573b.png)

