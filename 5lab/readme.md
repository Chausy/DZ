### Лабораторная работа. Доступ к сетевым устройствам по протоколу SSH

### Топология
![](https://github.com/Chausy/DZ/blob/94938b8ebf577308a8f2c5fe566e13cd6a84ac2c/5lab%20screen/%D1%82%D0%BE%D0%BF%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D1%8F.PNG)

### Таблица адресации
![](https://github.com/Chausy/DZ/blob/94938b8ebf577308a8f2c5fe566e13cd6a84ac2c/5lab%20screen/%D0%A2%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%20%D0%B0%D0%B4%D1%80%D0%B5%D1%81%D0%B0%D1%86%D0%B8%D0%B8.PNG)  


### Ход работы:  
# Выполним  настройку маршрутизатора  
![](https://github.com/Chausy/DZ/blob/94938b8ebf577308a8f2c5fe566e13cd6a84ac2c/5lab%20screen/%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D0%B8%20R1%20(1).PNG)  
![](https://github.com/Chausy/DZ/blob/94938b8ebf577308a8f2c5fe566e13cd6a84ac2c/5lab%20screen/%D0%BF%D0%B0%D1%80%D0%BE%D0%BB%D0%B8%20R1%20(2).PNG)  
![](https://github.com/Chausy/DZ/blob/94938b8ebf577308a8f2c5fe566e13cd6a84ac2c/5lab%20screen/%D0%BF%D0%BE%D0%B4%D0%BD%D1%8F%D0%BB%20%D0%B8%D0%BD%D1%82%D0%B5%D1%80%D1%84%D0%B5%D0%B9%D1%81%20R1.PNG)  





# Выполним базовую настройку для первого коммутатора S1
![](https://github.com/Chausy/DZ/blob/2affe29a1fdd636d560d06ad9918cb96c648e5fc/4lab%20screens/%D0%B2%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BD%D0%B0%20%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B5%20ipv6.PNG)  
![](https://github.com/Chausy/DZ/blob/48bb34987974569d48a96facbe860451de470259/4lab%20screens/%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20S1%20ipv6.PNG)
  
### Выполнение команды на R1 show ipv6 interface brief  
![](https://github.com/Chausy/DZ/blob/2affe29a1fdd636d560d06ad9918cb96c648e5fc/4lab%20screens/show%20ipv6%20interface%20brief.PNG)  


### Проверка сквозного подключения  
С PC-A отправил эхо-запрос на FE80::1. Это локальный адрес канала, назначенный G0/1 на R1  
![](https://github.com/Chausy/DZ/blob/2affe29a1fdd636d560d06ad9918cb96c648e5fc/4lab%20screens/PING%20c%20PC-A%20%D0%BD%D0%B0%20%D1%88%D0%BB%D1%8E%D0%B7%20%D0%BF%D0%BE%20%D1%83%D0%BC%D0%BE%D0%BB%D1%87%D0%B0%D0%BD%D0%B8%D1%8EPNG.PNG)  

Ввел команду tracert на PC-A, чтобы проверить наличие сквозного подключения к PC-B  
![](https://github.com/Chausy/DZ/blob/2affe29a1fdd636d560d06ad9918cb96c648e5fc/4lab%20screens/tracert.PNG)  
С PC-B отправил эхо-запрос на PC-A  
![](https://github.com/Chausy/DZ/blob/2affe29a1fdd636d560d06ad9918cb96c648e5fc/4lab%20screens/ping%20PC-A%20%D0%BD%D0%B0%20PC-B.PNG)  
С PC-B отправил эхо-запрос на локальный адрес канала G0/0 на R1  
![](https://github.com/Chausy/DZ/blob/2affe29a1fdd636d560d06ad9918cb96c648e5fc/4lab%20screens/ping%20PC-B%20%D0%BD%D0%B0%20G00.PNG)  















