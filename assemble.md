СБОРКА СХЕМЫ
===

Схема условно делится на несколько частей:

* Блок питания 
* Основная схема 
* Блок управления

![Image](https://github.com/minsk-hackerspace/Robbal/blob/master/images/Robbal_bp.png)

Схему можно собирать несколькими разными способами:

- Собрать на бесконтактной макетке

- Спаять на печатной макетной плате 

- Спаять модули проводами с некоторыми раззъемными соединениями

Сборка последним способом показанв на картинках ниже.

Сборка блока питания:
---

Блок питания это отсек с аккумуляторами и DC-DC преобразователь. Опционально можно добавить выключатель и модуль вольтметра чтобы видеть когда пора заряжать аккумуляторы. После спайки обязательно отрегулировать DC-DC модуль на стабилизированные +3.3В.
Так же сам DC-DC и дополнительные кнопку и вольтметр кремятся с помощью термопистолета на отсек.

В результате сборки блока питания зз него должно выходить три(четыре) провода:

- Нестабилизированные +11.7 В для питания двигателей. 
- Стабилизированные +3.3В для питания всей логики. 
- Земля одна или два провода.

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9024.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9025.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9025.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9026.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9028.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9029.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9031.jpg)


Сборка основной схемы:
---




Сборка блока управления:
---

Блок управления - это модуль HC-05 распаяный на переходную платку. 
Так же удобно к нему иметь 4х жильный провод мама-мама чтобы подсоединять его напрямую к разъему на Arduino.
Подсоединяется он туда только после того [блютус модуль настроен](https://github.com/minsk-hackerspace/Robbal/blob/master/bt.md) а сама [схема откалибрована](https://github.com/minsk-hackerspace/Robbal/blob/master/tune.md)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9033.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9034.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9035.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_0206.jpg)

