#### Устанавливаем зависимости
```
dep ensure
```

#### Поднимаем контейнер, из которого планируем писать логи
```
docker-compose up -d
```

#### Поднимаем логгер вместе с зависимостями
```
docker-compose -f docker-compose.logging.yaml up -d
```
Я выделил в отдельную подсеть *default* инфраструру graylog,
при этом из основной подсети сам сервис будет доступен по статически заданному IP *11.12.0.5*.

#### Настраиваем *input*
1. Открываем в браузере [http://localhost:9000](http://localhost:9000)
2. Вводим admin/admin (необходимо сменить через хеш в конфиге)
3. Переходим во вкладку *system->inputs*
4. Выбираем *GELF UDP*
5. Указываем название индекса


