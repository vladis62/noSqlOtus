#Redis

1. Key-value БД.
2. Данные хранятся в оперативной памяти
3. Однопоточность (отсутствие взаимных блокировок, атомарность транзакций)
4. Разнообразные структуры данных (строки, хэш-таблицы, списки, множества, упорядоченные множества)

___
## Домашнее задание

1. сохранить большой json (~20МБ) в виде разных структур - строка, hset, zset, list;
2. протестировать скорость

Решение:
1. Запустил в докере редис. На уровне с этим проектом файл - docker-compose.yml
2. Сохранил как строку, hset, zset и list - json из файла ./file.jso. Для сохранения пробовал использовать cli, оказалось плохой затеей, т.к. файл долго ставлявлялся и анализировать было вставку было неудобно.
Решил написать небольшую прогу и проанализировать работу сохраняя файл. В качестве либки редиса использовал `org.redisson:redisson:3.15.4`. На гитхаб саму прогу не заливал, в случае необходимости пришлю ссылку на проект.