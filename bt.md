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
Модуль необходимо припапять на плату
![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_8934.jpg)
Должно получится что-то такое:
![Image](https://raw.githubusercontent.com/minsk-hackerspace/Robbal/master/images/DSC_8984.jpg)



- [Мануал/даташит по модулю HC-05](https://www.gme.cz/data/attachments/dsh.772-148.1.pdf)
