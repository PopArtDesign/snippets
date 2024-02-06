#  Установка MailHog для MAMP (MacOS) 

1. Установить и запустить [MailHog](https://github.com/mailhog/MailHog)

   ```sh
    brew install mailhog
    brew services start mailhog
   ```

2. Добавить настройки в файл `/Applications/MAMP/bin/php/{PHP_VERSION}/conf/php.ini`

   Метки `{PHP_VERSION}` и `{MAILHOG_VERSION}` заменить на соответствующие версии

   ```ini
   [mail function]
   sendmail_path=/usr/local/Cellar/mailhog/{MAILHOG_VERSION}/bin/MailHog/sendmail
   ```

3. Открыть веб-интерфейс MailHog: [http://127.0.0.1:8025/](http://127.0.0.1:8025/)

4. Возможно, лучше перезагрузить систему полностью (перезагрузки MAMP бывает не достаточно)
