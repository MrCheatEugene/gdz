# ГДЗ в кармане?
ну, почти

## Вызов принят
Этот проект был создан когда мне кто-то скинул [этот тикток](https://youtu.be/l5UoIq3z8iU).

Такой хэлоу ворлд я делал в 7 лет.

Ну, и вот.. Почему бы и да?
## Как работает?
В качестве платформы нашей мини-читалки используетеся Ramps 1.4 и RepRap Discount Smart Controller.
> По сути, этот проект можно построить и без Ramps, но у меня завалялись компоненты от 3д принтера, и я их решил применить здесь.

Как говорит интернет - только велкий Марлин может работать с Ramps 1.4 и RepRap Discount Smart Controller, но что-то говорит мне об обратном..
## Немного кода для тех кому лень скачивать и воровать
```
const int rs = 16, en = 17, d4 = 23, d5 = 25, d6 = 27, d7 = 29;//дисплей
//я тут не написал, но 37 пин - пин пищалки
#define CLK 31// clock pin of encoder | clock энкодера
#define DT 33// DT энкодера | DT encoder pin
#define SW 35// кнопка энкодера | encoder switch
#define SDPIN 53 // sd cardreader pin (for ramps 1.4+reprap discount smart controller,not full graphics - 53 )
#include <LiquidCrystal.h>// И ДА, ДЛЯ ДИСПЛЕЯ МОЖНО ИСПОЛЬЗОВАТЬ ЭТУ БИБЛИОТЕКУ, А ПОД КАРДРИДЕР - ЭТУ
#include <SPI.h>
#include <SD.h>
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);
//ваш код...
```
Воруйте на здоровье.
И да, марлин не такая уже и магическая прошивка.
## Сборка

- Подключаем RepRap Discount Smart Controller через "смарт-адаптер" к RepRap шилду
- Подключаем шилд к Ардуино Мега
- Загружаем прошивку(загружается на 1.8.9 и выше)
- Загружаем файл gdz.txt согласно СИНТАКСИСУ(О НЁМ ПОЗЖЕ) на карту
- Вставляем карту
- Включаем

ВСЁ.
Или качаем автоматический установщик! Ссылка ниже.
## Синтаксис
### English, Русский
Max line length is 20 chars.
Максимальная длинна строки - 20 символов
### English VR
Max line length is 9 chars, and there should be double-space between the line,like

```Sample te||Sample te```

where ```|``` symbol is space
## Конфигурация
Если вы используете другие компоненты, или хотите сменить язык - отредактируйте конфиг.
Он находится чуть ниже заметок.
## Скачать
[Скачать автоматический установщик](https://github.com/MrCheatEugene/gdz/releases/download/1.0-fwuploader/fwu.zip)

[Скачать новейшую версию](https://github.com/MrCheatEugene/gdz/releases/latest/download/gdz.ino)

[Скачать первую версию](https://github.com/MrCheatEugene/gdz/releases/download/1.0/gdz.ino)
## Туториал
[Туториал на русском](https://youtu.be/WWX7OhSQuh8)
