# ГДЗ в кармане?
ну, почти

## Как работает?
В качестве платформы нашей мини-читалки используетеся Ramps 1.4 и RepRap Discount Smart Controller.
> По сути, этот проект можно построить и без Ramps, но у меня завалялись компоненты от 3д принтера, и я их решил применить здесь.

## Немного кода для тех кому лень скачивать и воровать
```

const int rs = 16, en = 17, d4 = 23, d5 = 25, d6 = 27, d7 = 29;//дисплей
//я тут не написал, но 37 пин - пин пищалки
#define CLK 31// clock pin of encoder | clock энкодера
#define DT 33// DT энкодера | DT encoder pin
#define SW 35// кнопка энкодера | encoder switch
#define SDPIN 53 // sd cardreader pin (for ramps 1.4+reprap discount smart controller,not full graphics - 53 )
#include <LiquidCrystal.h>
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);


```
