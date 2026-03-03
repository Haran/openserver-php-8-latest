### Что это

Это дополнительные модули для OSPanel / OpenServer Panel версий 5.2.х с поддержкой новых версий PHP.

### Credits

- **SagePtr**<br>Автор идеи и модуля PHP 8.3: [https://github.com/SagePtr/openserver-php-8.3](https://github.com/SagePtr/openserver-php-8.3)<br><br>
- **Gemorroj**<br>Много кастомных модулей включая бд: [https://github.com/Gemorroj/openserver](https://github.com/SagePtr/openserver-php-8.3)

### Что внутри

- PHP 8.3
- PHP 8.4
- PHP 8.5
- Composer 2.9.3 (с поддержкой до php 8.5)
- Apache 2.4.66

### Как использовать

- Если вы уже использовали модули от SagePtr, копируйте частично только нужные версии и http/Apache
- В противном случае просто скопируйте содержимое репозитория поверх установленного OSPanel 5.x
- Перезапустите OSPanel, в настройках сервера появятся новые версии PHP и HTTP

### На что обратить внимание

- _PHP 8.4 и 8.5 требуют обновлённого Apache_<br>Если при запуске сервера httpd.exe выбрасывает ошибку `The procedure entry point SSL_get0_group_name could not be located in the dynamic link library php_curl.dll` - вы используете несовместимую версию Apache. Да, несмотря на то, что обновление минорное, именно оно позволяет работать с PHP 8.4 и 8.5<br><br>
- _Чтобы кастомизировать свой домен (виртуалхост)_:<br>
  Cкопируйте `./userdata/config/Apache_2.4-PHP_8.4-8.5_vhost.conf` в корень домена, измените файл по необходимости и перезапустите сервер<br><br>
- _Composer перезаписывается обновлением_<br>
  Это может нарушить его работу со очень старыми версиями PHP. До версии 7.2 работоспособность сохраняется.<br><br>
- _Обновление NGinx пока не включено_<br>
  Доступен только Apache в одиночном варианте<br><br>

### ЧаВо

<dl>
<dt>The procedure entry point SSL_get0_group_name could not be located in the dynamic link library php_curl.dll</dt>
<dd>Вы используете несовместимую версию http/Apache</dd>
<dt>Почему не сделать PR обратно?</dt><dd>Я добавил Git LFS поверх уже существующего форка, а это перезаписывает все коммиты в истории</dd>
<dt>Есть OSPanel 6, зачем всё это?</dt><dd>Нравится OSPanel 6 - используйте его. Для меня он сломал всю идею - рабочая сборка из коробки в один клик, без ковыряния в конфигах</dd>
</dl>
