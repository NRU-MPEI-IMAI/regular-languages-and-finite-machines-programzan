# Дисциплина: "Теоретические модели вычислений"

## ИВТИ | А-13а-19 | Рамазанов Никита

### ДЗ №1. Регулярные языки и конечные автоматы.

**Задачи.**
1. Построить конечный автомат, распознающий язык;
2. Построить конечный автомат, используя прямое произведение;
3. Построить минимальный ДКА по регулярному выражению;
4. Определить, является ли язык регулярным;
5. Реализовать алгоритмы.

#### Задача 1. Построить конечный автомат, распознающий язык.

*NB: Автомат должен быть детерминированным.*

1. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7Bw%20%5Cin%20%5C%7Ba,b,c%20%5C%7D%5E*%20%7C%20%7Cw%7C_c%20=%201%20%5C%7D)

![Screenshot_1.png](attachment:Screenshot_1.png)

2. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7Bw%20%5Cin%20%5C%7Ba,b%5C%7D%5E*%20%7C%20%7Cw%7C_a%20%5Cleq%202;%20%7Cw%7C_b%20%5Cgeq%202%5C%7D)

![Screenshot_10.png](attachment:Screenshot_10.png)

3. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7Bw%20%5Cin%20%5C%7Ba,b%5C%7D%5E*%20%7C%20%7Cw%7C_a%20%5Cneq%20%7Cw%7C_b%20%5C%7D)

Условие, при котором автомат работает корректно - a и b чередуются, в противном случае построить ДКА нельзя.

![Screenshot_11.png](attachment:Screenshot_11.png)

4. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7Bw%20%5Cin%20%5C%7Ba,b%5C%7D%5E*%20%7C%20ww%20=%20www%20%5C%7D)

![Screenshot_12.png](attachment:Screenshot_12.png)

#### Задача 2. Построить конечный автомат, используя прямое произведение.

*NB: Автомат должен быть построен с помощью прямого произведения ДКА и его свойств.*

1. ![](https://latex.codecogs.com/svg.image?L_1%20=%20%5C%7Bw%20%5Cin%20%5C%7Ba,%20b%5C%7D%5E*%7C%20%7Cw%7C_a%20%5Cgeq%202%20%5Cwedge%20%7Cw%7C_b%20%5Cgeq%202%5C%7D)

![Screenshot_13.png](attachment:Screenshot_13.png)

2. ![](https://latex.codecogs.com/svg.image?L_2%20=%20%5C%7Bw%20%5Cin%20%5C%7Ba,%20b%5C%7D%5E*%7C%20%7Cw%7C_a%20%5Cgeq%203%20%5Cwedge%20%7Cw%7C_b%20%5Ctextup%7B%20is%20odd%7D%5C%7D)

![Screenshot_14.png](attachment:Screenshot_14.png)

3. ![](https://latex.codecogs.com/svg.image?L_3%20=%20%5C%7Bw%20%5Cin%20%5C%7Ba,%20b%5C%7D%5E*%7C%20%7Cw%7C_a%20%5Ctextup%7B%20is%20even%7D%20%5Cwedge%20%7Cw%7C_b%20%5Ctextup%7B%20multiple%20of%203%7D%5C%7D)

![Screenshot_15.png](attachment:Screenshot_15.png)

4. ![](https://latex.codecogs.com/svg.image?L_4%20=%20%5Coverline%7BL_3%7D)

![Screenshot_16.png](attachment:Screenshot_16.png)

#### Задача 3. Построить минимальный ДКА по регулярному выражению.

1. ![](https://latex.codecogs.com/svg.image?(ab&plus;aba)%5E*a)

![Screenshot_17.png](attachment:Screenshot_17.png)

2. ![](https://latex.codecogs.com/svg.image?a(a(ab)%5E*b)%5E*(ab)%5E*)

![Screenshot_18.png](attachment:Screenshot_18.png)

3. ![](https://latex.codecogs.com/svg.image?(a&plus;(a&plus;b)(a&plus;b)b)%5E*)

![Screenshot_19.png](attachment:Screenshot_19.png)

4. ![](https://latex.codecogs.com/svg.image?(b&plus;c)((ab)%5E*c&plus;(ba)%5E*)%5E*)

![Screenshot_20.png](attachment:Screenshot_20.png)

#### Задача 4. Определить, является ли язык регулярным.

Лемма о накачке:
![](https://latex.codecogs.com/svg.image?L-%5Ctext%7Bregular%7D%5CRightarrow%20%5Cexists%20n%5C;%5C;%5C;%5Cforall%20%5Comega%20%5Cin%20L,%5C;%5C;%5Cleft%7C%5Comega%5Cright%7C%5Cgeqslant%20n%5C;%5C;%5C;%5Cexists%20x,y,z%5C;%5C;%5C;%5Comega%20=xyz%5C;%5C;%5C;%5Cleft%7Cxy%5Cright%7C%5Cleqslant%20n%5C;%5C;%5C;%5C%5Cy%5Cneq%20%5Cvarepsilon%20%5C;%5C;%5C;%5Cforall%20i%5Cgeqslant%200%5C;%5C;%5C;xy%5Eiz%5Cin%20L)

Ее отрицание:
![](https://latex.codecogs.com/svg.image?%5Cforall%20n%5C;%5C;%5C;%5Cexists%20%5Comega%20%5Cin%20L,%5C;%5C;%5Cleft%7C%5Comega%5Cright%7C%5Cgeqslant%20n%5C;%5C;%5C;%5Cforall%20x,y,z%5C;%5C;%5C;%5Comega%20=xyz%5C;%5C;%5C;%5Cleft%7Cxy%5Cright%7C%5Cleqslant%20n%5C;%5C;%5C;%5C%5Cy%5Cneq%20%5Cvarepsilon%20%5C;%5C;%5C;%5Cexists%20i%5Cgeqslant%200%5C;%5C;%5C;xy%5Eiz%5Cnotin%20%20L)

1. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7B(aab)%5Enb(aba)%5Em%20%5Cmid%20n%20%5Cgeq%20%200,%20m%20%5Cgeq%20%200%5C%7D)

*Язык является регулярным.*

![Screenshot_21.png](attachment:Screenshot_21.png)

2. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7Buaav%20%5Cmid%20u%20%5Cin%20%5C%7Ba,%20b%5C%7D%5E*,%20v%20%5Cin%20%5C%7Ba,%20b%5C%7D%5E*,%20%7Cu%7C_b%20%5Cgeqslant%20%7Cv%7C_a%5C%7D)

Возьмем слово:
![](https://latex.codecogs.com/svg.image?%5Comega%20=%20b%5Enaaa%5En,%20%5Cforall%20n%5C%5C%5Cleft%7C%5Comega%20%20%5Cright%7C=2n&plus;2%20%5Cgeqslant%20n)

Тогда:
![](https://latex.codecogs.com/svg.image?xy=b%5Ekb%5Em,%20%5C:%5C:k&plus;m%5Cleq%20n,%20%5C:%5C:m%5Cneq%200%5C%5C%5Comega%20=b%5Ekb%5Emb%5E%7Bn-k-m%7Daaa%5En)

Накачиваем y:
![](https://latex.codecogs.com/svg.image?%5Comega%20=b%5Ek(b%5Em)%5Eib%5E%7Bn-k-m%7Daaa%5En%5C%5Ci=0%5C;%5C;%5CRightarrow%20%5C;%5C;%20%5Comega_0%20=b%5E%7Bn-m%7Daaa%5En%5C%5Cm%5Cneq%200%5C;%5C;%5CRightarrow%20%5Comega_0%5Cnotin%20L%20)

*Язык не является регулярным*

3. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7Ba%5Emw%20%5Cmid%20w%20%5Cin%20%5C%7Ba,%20b%5C%7D%5E*,%201%20%5Cleqslant%20%7Cw%7C_b%20%5Cleqslant%20m%5C%7D%20)

Возьмем слово:
![](https://latex.codecogs.com/svg.image?%5Comega%20=%20a%5Enb%5En,%20%5Cforall%20n%5C%5C%5Cleft%7C%5Comega%20%20%5Cright%7C%20%5Cgeqslant%20n)

Тогда:
![](https://latex.codecogs.com/svg.image?xy=a%5Eka%5Em,%20%5C:%5C:k&plus;m%5Cleq%20n,%20%5C:%5C:m%5Cneq%200%5C%5C%5Comega%20=a%5Eka%5Ema%5E%7Bn-k-m%7Db%5En)

Накачиваем y:
![](https://latex.codecogs.com/svg.image?%5Comega%20=a%5Ek(a%5Em)%5Eia%5E%7Bn-k-m%7Db%5En%5C%5Ci=0%5C;%5C;%5CRightarrow%20%5C;%5C;%20%5Comega_0%20=a%5E%7Bn-m%7Db%5En%5C%5Cm%5Cneq%200%5C;%5C;%5CRightarrow%20%5Comega_0%5Cnotin%20L)

*Язык не является регулярным*

4. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7Ba%5Ekb%5Ema%5En%20%5Cmid%20k%20=%20n%20%5Cvee%20m%20%3E%200%5C%7D)

Возьмем слово:
![](https://latex.codecogs.com/svg.image?%5Comega%20=%20a%5Enba%5En,%20%5Cforall%20n%5C%5C%5Cleft%7C%5Comega%20%20%5Cright%7C%20%5Cgeqslant%20n)

Тогда:
![](https://latex.codecogs.com/svg.image?xy=a%5Eka%5Em,%20%5C:%5C:k&plus;m%5Cleq%20n,%20%5C:%5C:m%5Cneq%200%5C%5C%5Comega%20=a%5Eka%5Ema%5E%7Bn-k-m%7Dba%5En)

Накачиваем y:
![](https://latex.codecogs.com/svg.image?%5Comega%20=a%5Ek(a%5Em)%5Eia%5E%7Bn-k-m%7Dba%5En%5C%5Ci=2%5C;%5C;%5CRightarrow%20%5C;%5C;%20%5Comega_2%20=a%5E%7Bn&plus;m%7Dba%5En%5C%5Cm%5Cneq%200%5C;%5C;%5CRightarrow%20%5Comega_2%5Cnotin%20L)

*Язык не является регулярным*

5. ![](https://latex.codecogs.com/svg.image?L%20=%20%5C%7Bucv%20%5Cmid%20u%20%5Cin%20%5C%7Ba,%20b%5C%7D%5E*,%20v%20%5Cin%20%5C%7Ba,%20b%5C%7D%5E*,%20u%20%5Cneq%20v%5ER%5C%7D)

Возьмем слово:
![](https://latex.codecogs.com/svg.image?%5Comega%20=%20(ab)%5Enc(ab)%5En%20=%20s_1s_2...s_n...s_%7B2n%7D...s_%7B4n%7Ds_%7B4n&plus;1%7D,%20%5Cforall%20n%5C%5C%5Cleft%7C%5Comega%20%20%5Cright%7C%20%5Cgeqslant%20n)

Тогда:
![](https://latex.codecogs.com/svg.image?xy=(s_1s_2...s_k)(s_%7Bk&plus;1%7Ds_%7Bk&plus;2%7D...s_%7Bk&plus;m%7D),%20%5C:%5C:k&plus;m%5Cleq%20n,%20%5C:%5C:m%5Cneq%200%5C%5C%5Comega%20=(s_1s_2...s_k)(s_%7Bk&plus;1%7Ds_%7Bk&plus;2%7D...s_%7Bk&plus;m%7D)(s_%7Bk&plus;m&plus;1%7Ds_%7Bk&plus;m&plus;2%7D...s_%7B2n%7Dc(ab)%5En))

Накачиваем y:
![](https://latex.codecogs.com/svg.image?%5Comega%20=(s_1s_2...s_k)(s_%7Bk&plus;1%7Ds_%7Bk&plus;2%7D...s_%7Bk&plus;m%7D)%5Ei(s_%7Bk&plus;m&plus;1%7Ds_%7Bk&plus;m&plus;2%7D...s_%7B2n%7Dc(ab)%5En)%5C%5Ci=2%5C;%5C;%5CRightarrow%20%5C;%5C;%20%5Comega_2%20=(s_1s_2...s_k)(s_%7Bk&plus;1%7Ds_%7Bk&plus;2%7D...s_%7Bk&plus;m%7D)%5E2(s_%7Bk&plus;m&plus;1%7Ds_%7Bk&plus;m&plus;2%7D...s_%7B2n%7Dc(ab)%5En)%5C%5Cm%5Cneq%200%5C;%5C;%5CRightarrow%20%5Comega_2%5Cnotin%20L)

*Язык не является регулярным*
