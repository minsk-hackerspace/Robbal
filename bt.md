Программирование BT модуля
===

Управление
---

Управление роботом осуществляется по bluetooth.
В качестве контроллера будет выступать любой Android смартфон с программой
Программа можете быть любая которая позволяет посылать настраиваеые команды на bloototh
В Play Market таких великое множество, например:

- [Arduino RC](https://play.google.com/store/apps/details?id=eu.jahnestacado.arduinorc)

- [Gadget Controller](https://play.google.com/store/apps/details?id=com.krio.gadgetcontroller)

Приемником управления будет выступать блютус модуль HC-05
Он позволит принять ваши команды управления из Андроид сматрфона и отдать их в роботу ардуину.

Блютус модуль в наборе поставляется в виде распространенного модуля HC-05 и переходной платки.
Платка позволяет втыкать его в макетку и питать от напряжения 5в (хотя логические уровни по прежнему остаются 3.3 вольта)
Так же на плате есть кнопка позволяющая перевести модуль в режим AT команд, зачем описано ниже.

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_8933.jpg)

Модуль необходимо припапять на плату вот таким вот образом:
![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_8934.jpg)

Должно получится что-то такое:
![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_8984.jpg)

Далее необходимо настроить модуль под свои нужны. Все модули по дефолту имеют одинаковое имя и пароль, а так-же дефолтная скорость всего 9600 бод.

Для этого модуль подсоединяется к любому USB-UART переходнику, на нем джамперои или переключателем выставляется напряжение 3.3 вольта. USB-UART через USB подключается к компьютеру с Ardiono IDE

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_8991.jpg)

Подключение такое:

UART | HC-05
--- | ---
GND | GND
VCC | +5v
TX | RX
RX | TX

Настройка происходит через Arduino IDE - Serial Monitor (Монитор порта) 
Туда пишутся команды, а модуль как-то на них отвечает.
Чтобы зайти в AT режим необходимо подключать модуль с нажатой кнопкой на переходной платке.
В Serial Monitor необзодимо выставить скорость 38400 и перевод строки Both NL & CR (это стандартно для AT режима) 

![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/Screen_29.png)

Команда | Значение
--- | ---
AT | пустой запрос ответом должен быть OK
AT+NAME? | спросить имя модуля
AT+NAME=Robbal | задать имя модуля Robbal
AT+PSWD? | спросить пин код
AT+PSWD="1122" | Задать пин код 1122
AT+UART=115200,0,0 | Задать скорость уарт 115200 бод
AT+RESET | перезагрузка и выход из AT режима

Примерный листинг (лог) команд которым настраивается модуль с запросами и ответами.
```
> AT
< OK
> AT+NAME?
< +NAME:HC-05
> AT+NAME=Robbal
< OK
> AT+NAME?
< +NAME:Robbal
> AT+PSWD?
< +PIN:"1234"
> AT+PSWD="1122"
< OK
> AT+PSWD?
< +PIN:"1122"
> AT+ROLE?
< +ROLE:0
> AT+UART?
< +UART:9600,0,0
> AT+UART=115200,0,0
< OK
> AT+UART?
< +UART:115200,0,0
> AT+RESET
< OK
```

- [Полный мануал/даташит по модулю HC-05](http://www.electronicaestudio.com/docs/istd016A.pdf)
