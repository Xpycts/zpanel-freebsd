Zpanel-freebsd
===============

Этот скрипт установит и сконфигурирует все необходимое для запуска ZpanelX

Пост в поддержку
http://blog.kogtev.com/configure-zpanel-on-freebsd-9-2/

Требования:
==============
*shell/bash  

Установка:
=========
mkdir -p /tmp/zpanelx && cd /tmp/zpanelx/  
fetch https://github.com/zpanel/zpanelx/archive/10.1.1.zip  
fetch https://github.com/Xpycts/zpanel-freebsd/archive/master.zip  
unzip -d . 10.1.1.zip && unzip master.zip  
cp -R zpanel-freebsd-master/* zpanelx-10.1.1/etc/build/  
rm -R zpanel-freebsd-master master.zip 10.1.1.zip  
cd zpanelx-10.1.1/etc/build/  
./new-install-BSD.sh  

После установки всех приложений установим пароль для админа  
./usr/local/etc/zpanel/panel/bin/setzadmin --set PASSWORD  

Что делает скрипт?  
===============  
1- Обновляем дерево портов  
2- Устанавливаем утилиту portupgrade  
2- Обновляем все установленные порты  
3- Устанавливаем все зависимости ZpanelX (apache, php, mysql, ...)  
4- Устанавливаем ZpanelX и конфигурируем её для работы.  

 Дополнения:  
=================  

Данный скрипт устанавливает все минимальные требования для работы ZpanelX, но он не устанавливает приложения для обеспечения безопасности (fail2ban, postscreen, amavisd, clamav ...).   


