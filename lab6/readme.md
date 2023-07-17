### Лабораторная работа. Доступ к сетевым устройствам по протоколу SSH

### Топология
![](https://github.com/Chausy/DZ/blob/16f6c3ef782bf6c04d918639e58396be96eab86c/lab6/%D1%82%D0%BE%D0%BF%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D1%8F.PNG)
![]([[https://github.com/Chausy/DZ/blob/94938b8ebf577308a8f2c5fe566e13cd6a84ac2c/5lab%20screen/%D1%82%D0%BE%D0%BF%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D1%8F.PNG](https://github.com/Chausy/DZ/blob/b42ac100d1492458d422974bfb4c6dae5fffa1f8/lab6/%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%20%D0%B0%D0%B4%D1%80%D0%B5%D1%81%D0%B0%D1%86%D0%B8%D0%B8.PNG))
![](https://github.com/Chausy/DZ/blob/e4948012c9349fb8ec8dd9d825ae1dd4b085405c/lab6/%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%20%D0%B2%D0%BB%D0%B0%D0%BD.PNG)



### Ход работы:  
# Выполним настройку коммутатора
![](https://github.com/Chausy/DZ/blob/c4353d1d71d425f0b8a23aad2e9ecc341dfc1752/lab6/%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BB%D0%B8%20vlan%20%D0%BD%D0%B0%20%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B5%2C%20%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D1%8F%D0%B5%D0%BC%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%BE%D0%B3%D0%B8%D1%87%D0%BD%D1%8B%D0%B5%20%D0%B4%D0%B5%D0%B9%D1%81%D1%82%D0%B2%D0%B8%D1%8F%20%D0%BD%D0%B0%20S2.PNG)  
# Так же выполняем действия и для второго коммутатора S2

# Выполним настройку PC
![](https://github.com/Chausy/DZ/blob/c4353d1d71d425f0b8a23aad2e9ecc341dfc1752/lab6/%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%B8%D0%BC%20Ip%20%D0%BA%D0%BE%D0%BC%D0%BF%D0%BE%D0%B2%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%BE%D0%B3%D0%B8%D1%87%D0%BD%D0%BE%D0%B3%D0%BE%20%D0%B4%D0%BB%D1%8F%20%D0%B2%D1%82%D0%BE%D1%80%D0%BE%D0%B3%D0%BE.PNG)   
# аналогично и для второго PC в соотвествии с таблицей

  
# Выполним настройку маршрутизатора R1
![](https://github.com/Chausy/DZ/blob/c4353d1d71d425f0b8a23aad2e9ecc341dfc1752/lab6/gjlbynthatqcs%20R1.PNG)  




### Настройка доступа через SSH на R1 
![](https://github.com/Chausy/DZ/blob/8d62f8efabda6d237bfb1a267b5592417663604e/5lab%20screen/%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%B5%D0%BC%20%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F%20%D0%B8%20%D0%B2%D0%BA%D0%BB%D1%8E%D1%87%D0%B0%D0%B5%D0%BC%20SSH%20R1.PNG)  

### Настройка доступа через SSH на S1
![](https://github.com/Chausy/DZ/blob/8d62f8efabda6d237bfb1a267b5592417663604e/5lab%20screen/%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0%20%D0%BA%D0%BE%D0%BC%D0%BC%D1%83%D1%82%D0%B0%D1%82%D0%BE%D1%80%D0%B0%20SSH.PNG)  


### подключение по SSH с PC-A на R1
![](https://github.com/Chausy/DZ/blob/8d62f8efabda6d237bfb1a267b5592417663604e/5lab%20screen/%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B8%D0%BB%D1%81%D1%8F%20%D0%BF%D0%BE%20SSH%20%D0%BD%D0%B0%20R1%20%D1%81%20PC%20%D1%81%20%D0%BB%D0%BE%D0%BA%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B9%20%D1%83%D1%87%D0%B5%D1%82%D0%BA%D0%B8.PNG)  


### подключение по SSH с PC-A на S1
![](https://github.com/Chausy/DZ/blob/8d62f8efabda6d237bfb1a267b5592417663604e/5lab%20screen/%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5%20%D0%BF%D0%BE%20SSH%20S1.PNG)  

### подключение по SSH с R1 на S1
![](https://github.com/Chausy/DZ/blob/8d62f8efabda6d237bfb1a267b5592417663604e/5lab%20screen/SSH%20S1%20%D0%BD%D0%B0%20R1.PNG)
