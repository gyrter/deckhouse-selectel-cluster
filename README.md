# Пример чарта для кластерных ресрсов

Чарт добавляет в кластер:
* Storage Class
* Ingress Controller
* Static User
* Dex auth


**HINT** Не забывайте сменить переменные на верные в `values.yaml` и `secret-values.yaml`. Это токены для доступа в Gitlab, пароль статичного пользователя.

**HINT** WERF_SECRET_KEY 5646f7fb2d19ea5a958476897d726877

# Работа с чартом

* Установить чарт после создания кластера
* Установить Deckhouse
* Запустить установку еще раз - тогда произойдёт установка кастомных ресурсов D8

# Генерация пароля статичного пользователя

```
echo "secret" | htpasswd -BinC 10 "" | cut -d: -f2
```
