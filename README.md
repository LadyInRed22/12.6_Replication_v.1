# Домашнее задание к занятию 12.6. «Репликация и масштабирование. Часть 1» - `Виноградова Татьяна`

## Задание 1

На лекции рассматривались режимы репликации master-slave, master-master, опишите их различия.

--- 

При репликации Master/Slave один узел используется для записи данных (Master), а остальные - только для чтения (Slave),
при репликации Master/Master все узлы являются ведущими, т.е. осуществляют и чтение, и запись данных. 
Master/Master является намного менее используемой, т.к. выход из строя одного из узлов практически неизбежно приводит к потере данных.
Репликация Master/Slave также является более предпочтительной из-за распределения нагрузки на БД (в силу своей архитектуры).

---

## Задание 2

Выполните конфигурацию master-slave репликации, примером можно пользоваться из лекции.

---
### Сервер 1:
#### Конфиг:
![image](https://user-images.githubusercontent.com/103531664/221381378-ee5b4611-c9ea-499e-aead-a169f83053e7.png)
---
#### Статус службы:
![image](https://user-images.githubusercontent.com/103531664/221381388-8810ba25-458f-42f8-8053-930c1005f235.png)
---
#### Статус мастера и создание тестовой БД:
![image](https://user-images.githubusercontent.com/103531664/221381429-15468c4c-8d49-4c7c-b718-3e09c1370b77.png)
---
### Сервер 2:
#### Конфиг:
![image](https://user-images.githubusercontent.com/103531664/221381463-b70d4b23-19a9-43fa-9f06-935b2df75ef2.png)
---
#### Статус службы:
![image](https://user-images.githubusercontent.com/103531664/221381474-524c3d13-ccf1-4890-90a8-f04e458caf29.png)
---
#### Статус слейва:
![image](https://user-images.githubusercontent.com/103531664/221381644-6afafc71-2a40-44de-82f1-2297c2610306.png)
![image](https://user-images.githubusercontent.com/103531664/221381651-7e5398df-fc4c-47f9-b10f-9ce9465ddf18.png)
---
#### Репликация тестовой БД:
![image](https://user-images.githubusercontent.com/103531664/221381698-58e9fdb4-7192-4abe-a4a0-a04e40aa9964.png)
---

## Задание 3* 

Выполните конфигурацию master-master репликации. Произведите проверку.

---
### Сервер 2:
#### Статус мастера:
![image](https://user-images.githubusercontent.com/103531664/221381802-21284ac8-8541-457a-b8f5-d2600d658f6f.png)
---
#### Создание тестовой БД_2:
![image](https://user-images.githubusercontent.com/103531664/221381858-9b5f1788-a2b0-4924-9065-b4c2e151a97f.png)
---
### Сервер 1:
#### Статус слейва:
![image](https://user-images.githubusercontent.com/103531664/221381918-1bc35da5-73ba-4c9f-8e46-83ae52ce9909.png)
![image](https://user-images.githubusercontent.com/103531664/221381940-6d20af5a-871c-4967-81a3-12f84bc64ded.png)
--- 
#### Репликация тестовой БД:
![image](https://user-images.githubusercontent.com/103531664/221381978-fd7ce265-37f8-41e8-a3cc-6e21c5c075d3.png)
---
