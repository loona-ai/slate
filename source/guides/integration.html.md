---
layout: integration
title: Integration Documentation

search: true
home: false
---
# iiko
## Установка плагина
- Копируем папку LoonaPluginSettings в C:\Users\YourUserName\ProgramData 

- Копируем папки LoonaPlugin и iikoWaiter5 в директорию iikoFront/Plugins (в нашем случае C:\Program Files\iiko\iikoRMS\Front.Net\Plugins)

- Запускаем iiko Front (помним что для данного метода нужна лицензии типа iikoTableService, iikoWaiter, iikoFrontPaymentPlugin)

- В iiko Front переходим в раздел “Дополнения” и выбираем “Loona settings”

- Введите Логин и Пароль

<img src="../images/iiko1.PNG" width="900">

- Задаем настройки:
        
   - Api access token - по запросу  
   - Api base url - https://api.loona.ai  
   - Waiter request url - http://localhost  
   - Waiter port - 1234
   
   <img src="../images/iiko2.png" width="512" height="288" alt="Card Flip">

- Открываем iiko Office
    - Переходим в раздел Дисконтная Система -> Скидки и Надбавки
    - Добавляем скидку
    - Обязательно пишем название - LoonaFixedSumDiscount
    - Тип скидки ставим Скидки и Надбавки
    - Нажимаем Далее
    
<img src="../images/iiko3.PNG" width="900">

- Убираем галочку Можно назначить вручную, остальное по усмотрению ресторана

<img src="../images/iiko4.png" width="800">

- Тип ставим “Фиксированная сумма” и обязательно устанавливаем галочку “Назначать сумму”

<img src="../images/iiko5.png" width="900">

- Нажимаем Далее и заканчиваем установку скидки.


- Добавляем внешний вид оплаты. Переходим в раздел “Розничные продажи”  нажимаем на “Тип платы” и добавляем новую оплату. 
- Обязательно указываем: 

    - Наименование - LoonaPayment  
    - Тип - Внешний тип оплаты  
    - Название в чеке - пишите что хотите  
    - Безналичный тип - Loona Payment
- Сохраняем

<img src="../images/iiko6.png" width="665">

- Устанавливаем мобильное приложение iikoWaiter5

- Перезагружаем iiko front

## Настройки в приложении

### Редактирование макета

Для использования скидок и бонусов в системе iiko штрихкод на карте должен содержать Номер Карты. Для настройки штрихкода на Номер Карты:

- Перейдите в раздел **Макеты**

- Зайдите в <img src="../images/иконка%20редактирования.png" width="12" height="12" alt="редактирование"> **редактирование** того макета на который хотите настроить сканер

<img src="../images/Number%20scanner.png" width="624">

- Перейдите в секцию **Дизайн**

- Нажмите на штрихкод, в настройках поля откроются настройки штрихкода

- Поменяйте значение на **Номер Карты**

Для использования купона:

- Обнаружить номер под которым продукта зарегистрирован в CRM системе

- В значении штрихкода поменять значение на “своё значение”

- Поменять своё значение на ${pid}/№Продукт, где “№Продукт” это номер под которым продукт зарегистрирован

- Использовать карты Loona

### Создание сканера для карты

Для использования системы iiko вам необходимо использовать создать сканер для получения идентификационного номера. Этот сканер будет необходим для пользования интегрированой системой с iiko․

Для создания нового сканера:

<img src="../images/maket_create.png" width="600">

- В разделе Сканер нажмите на Создать сканер.

- Введите название нового сканера

- Выберите тип сканера - "App".

- Выберите макеты с картами которые предназначены для сканирования, или отметьте Получить полный доступ чтобы сканер работал со всеми вашими макетами.

- Нажмите Создать

В списке созданных сканеров появится новый сканер со своим **Идентификационным номером**, этот номер используется при настройке плагина.

# r_keeper

## Установка плагина

*В течении использования плагина, нужно выключить Windows Firewall или открыть доступ для порта плагина (port 1234)

-	Скачайте и откройте папку плагина Loona

 <img src="../images/rk1.png" width="600" >

-	Скопируйте «Extdll.dll» и «Extdll.ini» в папку UCS/FARCARDS
 
 <img src="../images/rk2.png" width="550" >

-	Откройте файл «FARCARDS.INI» в текстовом редакторе

-	В поле DLL впишите «ExtDll.dll» и сохраните изменения
 
 <img src="../images/rk3.png" width="700">

-	Запустите  «Farcards.exe – install»

-	Откройте папку где содержится R-keeper и запустите R-keeper «Manager»
 
 <img src="../images/rk4.png" width="700">

-	Откройте систему r_keeper и зайдите в неё

-	Пройдите в меню в раздел «Деньги» и откройте «Скидки и Наценки»
 
 <img src="../images/rk5.png" width="900">

-	Откроется окно управления скидок и наценок, наведите мышь на поле «All» и с помощью правой кнопки мышки создайте новый тип скидок
 
 <img src="../images/rk6.png" width="900" height="350">

-	Откроются «Свойства», в них введите Название своей скидки и поменяйте статус на Активный
 
 <img src="../images/rk7.png" width="500">

-	Пройдите в окно «Скидки/Нацинки» вашей новой скидки и создайте новую скидку (Нажмите правой кнопки мышки на свободое поле, из возникших опций выберите «Новая скидка»)
 
 <img src="../images/rk8.png" width="900">

-	Введите название вашей скидки, пока что не меняйте статус на активный
 
 <img src="../images/rk9.png" width="900">

-	Откройте детализацию вашей скидки двойным кликом на иконку
 
 <img src="../images/rk10.png" width="414" height="150">

-	Создайте новую детализацию (Нажмите правой кнопки мышки на свободое поле, из возникших опций выберите «Новая детализация»)
 
 <img src="../images/rk11.png" width="345" height="347">

-	Откройте поле настроек детализации, и поменяйте процент скидки на 100.00
 
 <img src="../images/rk12.png" width="900">

-	Сохраните изменения 

 <img src="../images/rk13.png" width="900">

-	Пройдите обранто в «Свойства» вашей скидки и поменяйте статус на активный «Active»

 <img src="../images/rk14.png" width="900">

-	Сохраните изменения, но еще не закрывайте окно «Скидки и Надбавки»

-	Откройте папку Loona R-keeper

-	Скопируйте папку Loona в папку где хратится r_keeper и FARCARDS

 <img src="../images/rk15.png" width="750">

-	Откройте скопированую папку Loona, и запустите из нее файл «ServiceInstaller.exe» как администратор

 <img src="../images/rk16.png" width="700">

-	Сервис будет установлен, после установки зайдите в Windows  Services (Сервисы), найдите Loona r-keeper plugin и убедитесь что «Startup Type» стоит автоматичекий (Automatic)

 <img src="../images/rk17.png" width="900">

-	Не закрывайте окно сервисов

-   Далее, откройте r_keeper менеджер и пройдите в ***Сервисы -> Обработка Сигналов Устройств -> MCR алгоритмы***

<img src="../images/rk_extra1.PNG" width="900"> 

-   Откроется страничка существующих алгоритмов. Убедитесь что у вас имеется алгоритм loona.

<img src="../images/rk_extra2.PNG" width="900"> 

-   В случае если у вас нет этого алгоритма, создайте новый.

-   Для создания нового алгоритма можно просто скопировать любой имеющийся алгоритм и вставить его в окно алгоритмов. 

<img src="../images/rk_extra_if1.PNG" width="600"> 

<img src="../images/rk_extra_if2.PNG" width="600"> 

-   После этого, у васбудет иметься 2 одинаковых алгоритма. Переименуйте один из них на **loona**.

-   Нажмите на алгоритм и откроются свойства справа, поменяйте статус на **Active** и затем убедитесь что все настройки совпадают с настройками представленными ниже:

<img src="../images/rk_extra_if3.png" width="900"> 

-   Нажмите на скрипт, и откройте окно скрипта с помощью иконки слева.

<img src="../images/rk_extra3.png" width="900"> 

-   В окне скрипта замените имеющийся скрипт на код расположенный ниже:


<pre><code>
function MCR1000028(DeviceSignal: Integer; DeviceIdent: Integer; var Parameter: String): Boolean;
var enc: integer; id, ratio, couponeCode :integer; 
var encShift, couponCodeShift :integer;
var couponSeparateSymbol :String;        
var idString:String;
var cardCodeResult:Int64;
begin 
 
  Result:=false;           
  ratio :=1000; 
  encShift :=48;
  couponCodeShift:=36;
  couponSeparateSymbol := '/';    

  if pos('-', Parameter) > 1 then begin
        Enc := StrToIntDef(copy(Parameter, 1, pos('-', Parameter) - 1),-1);
        if Enc>0 then begin
          idString := copy(Parameter, pos('-', Parameter)+1, length(Parameter));
          
           if pos(couponSeparateSymbol, idString) > 1 then begin
            couponeCode := StrToIntDef(copy(idString, pos(couponSeparateSymbol, idString)+1, length(idString)),-1);
            idString :=   copy(idString, 1, pos(couponSeparateSymbol, idString) - 1)       
          end; 

          id :=  StrToIntDef(idString,-1)-(enc-(enc/ratio)*ratio);
          cardCodeResult :=     (enc shl encShift ) and (StrToInt64('0x7FFF')shl encShift);
          cardCodeResult :=    cardCodeResult or ((couponeCode shl couponCodeShift) and (StrToInt64('0xFFF')shl couponCodeShift) ) ;
          cardCodeResult :=    cardCodeResult or id;
          Parameter :=Int64ToStr(cardCodeResult);
          Result:=true;     
        end;  
  end;       
end;
<img src="../images/rk_extra4.PNG" width="900"> 
</code></pre>

-   Нажмите "Ок" и закройте окно

-	Затем откройте ваш браузер

-	Введите адрес плагина в браузере, адрес: «localhost:1234/settings»

-	Откроется поле настроек плагина. Введите необходимые параметры для настройки скидки и сохраните параметры. Код вашей скидки вам доступен в свойствах скидки в r_keeper manager.
    
     - Для получения Идентификационного номера сканера и URL API приложения обратитесь к документации приложения Loona. В случае если URL приложения это "https://app.loona.ai", то URL API приложения это: "https://api.loona.ai".

     - При изменениях порта на «XXXX», адрес плагина меняется на localhost:XXXX/settings (но нет необходимости менять порт) 
     
<img src="../images/rk18.png" width="900"> 

<img src="../images/rk19.png" width="900">

-	Сохраните изменения параметров плагина

-	Вернитесь в «Сервисы», выделите сервис Loona r-keeper plugin, обновите сервис (сервис должен выключится после обновления), затем запустите сервис

 <img src="../images/rk20.png" width="900">

## Настройки в приложении

### Редактирование макета

Для использования скидок и бонусов в системе r_keeper штрихкод на карте должен содержать Номер Карты. Для настройки штрихкода на Номер Карты:

- Перейдите в раздел **Макеты**

- Зайдите в <img src="../images/иконка%20редактирования.png" width="12" height="12" alt="редактирование"> **редактирование** того макета на который хотите настроить сканер

<img src="../images/r_keeper%20maket%20settings.png" width="650" height="375" alt="Card Design">

- Перейдите в секцию **Дизайн**

- Нажмите на штрихкод, в настройках поля откроются настройки штрихкода

- Поменяйте тип штрихкода на QR

- Поменяйте значение на **Номер Карты**

### Создание сканера для карты

Для использования системы r_keeper вам необходимо использовать создать сканер для получения идентификационного номера. Этот сканер будет необходим для пользования интегрированой системой с iiko․

Для создания нового сканера:

<img src="../images/maket_create.png" width="600" alt="Maket Create">

- В разделе Сканер нажмите на Создать сканер.

- Введите название нового сканера

- Выберите тип сканера - "App".

- Выберите макеты с картами которые предназначены для сканирования, или отметьте Получить полный доступ чтобы сканер работал со всеми вашими макетами.

- Нажмите Создать

В списке созданных сканеров появится новый сканер со своим **Идентификационным номером**, этот номер используется при настройке плагина.
 