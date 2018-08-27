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

Основная схема это соедененные проводами Ардуина, шаговые драйвера и гироскоп.
Соединяется все по схеме достаточно просто с помощью небольшого количества проводков.
Для удобства немлохо иметь коннекторы к шаговым двигателям и на питание всей схемы. 

Из нюансов стоит обратить внимание и правильно подсоединить к драйверам пары обмоток шагового двигателя. 
На фотографиях обмотки это синий+желтый и красный+зеленый.

Так же можно предусмотреть перемычки для настройки микростеппинга на драйверах. Хорошо себя показали 1/2 и 1/4 микрошага.
При 1/2 можно развить большую скорость. При 1/4 движения более плавные, робот легче в настройке и меньше падает.

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9115.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9117.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9116.jpg)


Сборка блока управления:
---

Блок управления - это модуль HC-05 распаяный на переходную платку. 
Так же удобно к нему иметь 4х жильный провод мама-мама чтобы подсоединять его напрямую к разъему на Arduino.
Подсоединяется он туда только после того [блютус модуль настроен](https://github.com/minsk-hackerspace/Robbal/blob/master/bt.md), а сама [схема откалибрована](https://github.com/minsk-hackerspace/Robbal/blob/master/tune.md)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_8933.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_8935.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_9033.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_0206.jpg)


Крепление схемы в корпус
---
После спайки соединенные проводами модули крепится на термоклей внутрь корпуса.

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_0007.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_0008.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_0110.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_0111.jpg)

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_0141.jpg)
