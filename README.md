# Bugiman3d_infra
Bugiman3d Infra repository

1. Для подключения с помощью джамп-машины к хосту по внутреннем IP-адресу, используем следующую команду: ssh -i ~/.ssh/appuser -A -J appuser@"JUMP_HOST" appuser@"END_HOST"
2. Для подключения с помощью алиаса:

2.1 Создаём файл "config" в ~/.ssh со соедующими параметрами:

""""""""""""""""""""""""""""""""""
Host someinternalserver
HostName "END_HOST"
ProxyJump appuser@"JUMP_MACHINE"
User appuser
IdentityFIle ~/.ssh/appuser
""""""""""""""""""""""""""""""""""

2.2 Сохраняем его
2.3 Подключаемся через терминал с помощью следующей команды: ssh someinternalhost

3. Конфигурация и данные для подключения к bsation:
bastion_IP = 178.154.200.199
someinternalhost_IP = 10.129.0.5
