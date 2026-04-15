
# Задание 1

1. check
2. Проблемы:
    - отсутствие описания nemespace в манифесте
    - обращение из `web-consumer` в `auth-db` по короткому имени сервиса, хотя они в разных namespace
    - Порты в контейнерах без имени.
3. [Исправленный манифест](task.yaml)
    - Добавил создание двух **namespace** : `web` и `data`
    ```
    apiVersion: v1
    kind: Namespace
    metadata:
      name:  web
    ```
    - Обращение к **service** в другом **namespace** по полному имени `auth-db.data.svc.cluster.local`:
        ```
        command:
        - sh
        - -c
        - while true; do curl auth-db.data.svc.cluster.local; sleep 5; done
        ```
    - Именование порта контейнера **nginx** в поде **auth-db**
    ```
    ports:
    - name: http
      containerPort: 80
      protocol: TCP
    ```
4. [Скриншот логов пода web-consumer после исправления](screenshots/1.jpg)
