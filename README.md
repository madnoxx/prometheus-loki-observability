# prometheus-loki-observability

Полный стек мониторинга и логирования, развернутый через Docker Compose.

Проект включает:

- **Prometheus** + **Node Exporter** + **cAdvisor** — сбор метрик с хостов и контейнеров.
- **Alertmanager** — уведомления при критических событиях.
- **Grafana** — визуализация метрик и логов.
- **Loki** + **Promtail** — сбор, хранение и поиск логов.

Все сервисы запускаются через Docker Compose.

Этот проект нужен для того, чтобы:
- Собирать метрики хостов, контейнеров и приложений.
- Собирать логи и хранить их в централизованной базе.
- Отправлять уведомления при проблемах.
- Визуализировать всё через Grafana.

## Установка

1. Клонировать репозиторий:
```bash
git clone git@github.com:madnoxx/prometheus-loki-observability.git
cd prometheus-loki-observability
```
2. Создать .env и заполнить секреты
3. Запустить:
```bash
docker-compose up -d
```
4. Проверка состояния контейнеров:
```bash
docker-compose ps
```

## Использование

Grafana: http://localhost:3000
Prometheus: http://localhost:9090
Alertmanager: http://localhost:9093
Loki: http://localhost:3100
