# Задание 1

[containers-data-exchange.yaml](https://github.com/jaack1/netology-kuber/blob/main/2.1/containers-data-exchange.yaml)

![Image alt](https://github.com/jaack1/netology-kuber/blob/main/2.1/screenshots/1.png)

![Image alt](https://github.com/jaack1/netology-kuber/blob/main/2.1/screenshots/2.png)

# Задание 2

[pv-pvc.yaml](https://github.com/jaack1/netology-kuber/blob/main/2.1/pv-pvc.yaml)

![Image alt](https://github.com/jaack1/netology-kuber/blob/main/2.1/screenshots/3.png)

![Image alt](https://github.com/jaack1/netology-kuber/blob/main/2.1/screenshots/4.png)

В политике PV persistentVolumeReclaimPolicy установлено значение Retain, по этому PV остался на месте со статусом Released. Содержимое сохранилось, а в атрибуте Claim теперь записан PVC, с которым PV был связан. Если бы политика была delete, то данные внутри тома удалились бы, он бы перешёл в статус Available.

![Image alt](https://github.com/jaack1/netology-kuber/blob/main/2.1/screenshots/5.png)

После удаления PV, файл остался, по той же причине, потому что persistentVolumeReclaimPolicy = retain

# Задание 3

[sc.yaml](https://github.com/jaack1/netology-kuber/blob/main/2.1/sc.yaml)

![Image alt](https://github.com/jaack1/netology-kuber/blob/main/2.1/screenshots/6.png)