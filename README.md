# Отчёт о тестировании Credit Card Number Validator

## Краткое описание
07/04/2020 - 07/04/2020 было проведено тестирование методом черного ящика приложения Credit Card Number Validator

На тестирование затрачено: 3 часа

## В результате тестирования выявлены следующие дефекты:

[При вводе валидного номера карты, отличного от 16-значного, получаем результат `FAIL`](https://github.com/baskrasen/javaqa-homeworks-1-credit_card_number-_validator/issues/1)

## Описание процесса тестирования

### В процессе тестирования были проверены следующие данные:

| Проверяемые данные     | ФР              | ОР |
| ------------- |:------------------:| -----:|
| 15 цифр    | FAIL    | FAIL |
| 17 цифр    | FAIL |   FAIL |
| 16 русских букв  | FAIL         |    FAIL|
|16 латинских букв |FAIL |FAIL
|16 символов |FAIL |FAIL
|ничего |FAIL |FAIL
|валидный 16-значный VISA |OK |OK
|валидный 18-значный VISA |OK |FAIL
|валидный 16 значный Discover |OK |OK
|валидный 18 значный Discover |OK |FAIL
|валидный 14 значный Diners Club - Carte Blanche |OK |FAIL
|валидный 16 значный Visa Electron |OK |OK
|валидный 16 значный MasterCard |OK |OK
|валидный 14-зн. Diners Club - International |OK |FAIL
|валидный 15-зн. American Express (AMEX): |OK |FAIL

## В процессе тестирования использовались следующие артефакты:

1. [Руководство по установке IntelliJ IDEA](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/idea.md)
2. Генератор номеров кредитных карт и валидатор [Credit Card Number Generator & Validator](https://www.freeformatter.com/credit-card-number-generator-validator.html)

## В качестве тестовых данных использовались данные: 

1. [Сгенерированные валидные номера карт](https://www.freeformatter.com/credit-card-number-generator-validator.html)

   * 30437542846603 Diners Club - Carte Blanche
   * 36440187504846 Diners Club - International
   * 341049570537113 American Express (AMEX) 
   * 4404611274387973045 VISA
   * 6011216427023522994 Discover

   - эти валидные данные карт получили результат `FAIL`


## Тестирование производилось в следующем окружении:

1. Windows 10 v.1809
2. IntelliJ IDEA v.2019.3.4