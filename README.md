Zpanel-freebsd
===============
Version 0.1

Этот скрипт установит и сконфигурирует все необходимое для запуска ZpanelX


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


