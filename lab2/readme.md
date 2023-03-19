### Лабораторная работа. Базовая настройка коммутатора 
### 1) Топология
![](https://github.com/Chausy/DZ/blob/1a4b517aac11fcc4f7093a0751c0336050aacad6/screen%202lab/%D1%82%D0%BE%D0%BF%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D1%8F.PNG)
### Таблица адресации
![](https://github.com/Chausy/DZ/blob/65458582f721379ecbdfbb5c88e8919ab3e094ce/screen%202lab/%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%20%D0%B0%D0%B4%D1%80%D0%B5%D1%81%D0%B0%D1%86%D0%B8%D0%B8.PNG)  
###	Необходимые ресурсы  
•	2 коммутатора (Cisco 2960 с операционной системой Cisco IOS 15.2(2) (образ lanbasek9) или аналогичная модель)  
•	2 ПК (Windows и программа эмуляции терминала, такая как Tera Term)  
•	Консольные кабели для настройки устройств Cisco IOS через консольные порты  
•	Кабели Ethernet, расположенные в соответствии с топологией  

### Ход работы:  
![](https://github.com/Chausy/DZ/blob/b1da0b0c78118a7dc07b7e8cc94e8ce20545d005/%D0%BF%D0%BE%D0%B4%D1%81%D0%BE%D0%B5%D0%B4%D0%B8%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BA%D0%BE%D0%BD%D1%81%D0%BE%D0%BB%D1%8C%D0%BD%D1%8B%D0%BC%20%D0%BA%D0%B0%D0%B1%D0%B5%D0%BB%D0%B5%D0%BC.PNG)

# Выполним базовую настройку для первого коммутатора S1
1) Подсоединил консольный кабель от PC-A c порта RS 232 (COM) в порт console в коммутаторе S1  
2) Проверил настройки коммутатора по умолчанию  
3) Приступил к настройке базовых параметров коммутатора  
  
### В данном этапе присвоим имя коммутатору, так же задим пароли для входа в привелигированный режим и консольного подключения
Для этого с помощью консольного подключения с помощью эмуляции терминала:  
- Enable - перешел в привелигированный режим    
- conf t - перешел в режим глобальных настроек  
- hostname S1 - дал имя коммутатору  
- no ip domain-lookup - запретил нежелательный поиск в DNS   
- enable secret class - поставил пароль class на привелигированный режим  
- line console 0 - перешел в настройку консольного подключения  
- password cisco - задал пароль cisco на доступ консоль
- login - чтобы при подключении в консоль вывелось вести пароль  
- logging synchronous - чтобы консольные сообщения не прерывали выполнение команд    

![](https://github.com/Chausy/DZ/blob/e32e2e50ebfc27292621cf6edb1d113353a5759f/1.1.PNG)  
![](https://github.com/Chausy/DZ/blob/e32e2e50ebfc27292621cf6edb1d113353a5759f/1.2.PNG)  
 
### Установка баннера
Для этого с помощью консольного подключения с помощью эмуляции терминала: 
- conf t  
- banner motd *Unauthorized access is strictly prohibited. * - при подключении к консоли будем видеть данное сообщение  

![](https://github.com/Chausy/DZ/blob/e32e2e50ebfc27292621cf6edb1d113353a5759f/3.1.PNG)

### Зашифруем все пароли  
Для этого с помощью консольного подключения с помощью эмуляции терминала: 
- conf t  
- service password-encryption - для шифрования паролей (перевода в 16ричную СС)  

![](https://github.com/Chausy/DZ/blob/e32e2e50ebfc27292621cf6edb1d113353a5759f/4.1.PNG)  
![](https://github.com/Chausy/DZ/blob/e32e2e50ebfc27292621cf6edb1d113353a5759f/4.2.PNG)  

### Настройка канала виртуального соединения для удаленного управления (vty)  
Для этого с помощью консольного подключения с помощью эмуляции терминала: 
- conf t  
- line vty 0 4 - зашел на канал VTY  
- password cisco - поставил пароль для удаленного подключения
- login - чтобы при подключении в консоль вывелось вести пароль  
- logging synchronous - чтобы консольные сообщения не прерывали выполнение команд  
- transport input telnet - включаем протокол телнет для удаленного доступа к коммутатору

![](https://github.com/Chausy/DZ/blob/e32e2e50ebfc27292621cf6edb1d113353a5759f/6.1.PNG)  

### Настройка интерфейса  
Для этого с помощью консольного подключения с помощью эмуляции терминала: 
- conf t  
- interface vlan 1 - используем первый vlan  
- ip address 192.168.1.11 255.255.255.0 - присваем IP-адрес и маску коммутатору  
- no shutdown - включить интерфейс  

![](https://github.com/Chausy/DZ/blob/f7d56523d875510c5bc8342d31c3d88f841d0128/screen%202lab/ip%20S1.PNG)  

# Выполним базовую настройку для второго коммутатора S2
Настройка выполняется по аналогии с первым коммутатором S1, но поменяется IP-адрес второго коммутатора.  
Для этого с помощью консольного подключения с помощью эмуляции терминала: 
- conf t  
- interface vlan 1 - используем первый vlan  
- ip address 192.168.1.12 255.255.255.0 - присваем IP-адрес и маску коммутатору  
- no shutdown - включить интерфейс  

![](https://github.com/Chausy/DZ/blob/f7d56523d875510c5bc8342d31c3d88f841d0128/screen%202lab/ip%20S2.PNG)  


# Изучение таблицы МАС-адресов коммутатора  
Открыл командную строку на PC-A и ввел команду ipconfig /all

![](https://github.com/Chausy/DZ/blob/29e7355fe4ae992a45b92a3258e5d4dab36fca22/screen%202lab/ipconfig%20PC-A.PNG)  
MAC-адрес компьютера PC-A - физический адрес в скрине  

Подключился к коммутаторам S1 и S2 через консоль и ввел команды show interface F0/1 на каждом коммутаторе.
S1  
![](https://github.com/Chausy/DZ/blob/29e7355fe4ae992a45b92a3258e5d4dab36fca22/screen%202lab/show%20interface%20S1.PNG)  
S2  
![](https://github.com/Chausy/DZ/blob/29e7355fe4ae992a45b92a3258e5d4dab36fca22/screen%202lab/show%20interface%20S2.PNG)

### Просмотреть таблицу МАС-адресов коммутатора S2  
![](https://github.com/Chausy/DZ/blob/29e7355fe4ae992a45b92a3258e5d4dab36fca22/screen%202lab/show%20mac%20address-table%20S2.PNG)  

### Очистил таблицу МАС-адресов коммутатора S2 и снова отобразил таблицу МАС-адресов  
![](https://github.com/Chausy/DZ/blob/29e7355fe4ae992a45b92a3258e5d4dab36fca22/screen%202lab/%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20clear%20mac%20address-table%20dynamic%20S2.PNG)

### С компьютера PC-B отправил эхо-запросы устройствам в сети и просмотрел таблицу МАС-адресов коммутатора
На компьютере PC-B открыл командную строку и ввел команду arp -a, а так же выполнил эхо-запросы с ПК-А, S1, S2  
![](https://github.com/Chausy/DZ/blob/29e7355fe4ae992a45b92a3258e5d4dab36fca22/screen%202lab/arp%20%D0%B8%20%D1%8D%D1%85%D0%BE%20%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%20%D1%81%20PC-B.PNG)

После эхо-запроса выполним команду show mac address-table  
![](https://github.com/Chausy/DZ/blob/29e7355fe4ae992a45b92a3258e5d4dab36fca22/screen%202lab/%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%20%D1%8D%D1%85%D0%BE%20%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%BE%D0%B2%20%D1%81%20PC-B%20%D1%81%20%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B0%20S2%20show%20mac%20address-table.PNG)













