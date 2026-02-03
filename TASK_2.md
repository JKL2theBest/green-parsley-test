# Задание 2: Проектирование API для экрана "Магазины партнеров"

## Описание метода
**Цель:** Получение списка доступных магазинов-партнеров для отображения на экране выбора.

**Метод:** `GET`
**URL:** `/api/v1/partners/stores`

**Заголовки (Headers):**
*   `Content-Type: application/json`
*   `X-User-Location: {lat},{lon}` (Опционально: для расчета времени доставки конкретно для пользователя)

---

## Пример ответа (Response Body)

```json
{
  "stores": [
    {
      "id": 101,
      "name": "METRO",
      "logo_url": "https://cdn.petrushka.ru/logos/metro_v2.png",
      "target_url": "https://metro-cc.ru/delivery",
      "delivery_info": {
        "text": "Ближайшая доставка сегодня",
        "time_slot": "21:00-23:00",
        "is_express": false
      },
      "style": {
        "background_color": "#FFFFFF",
        "text_color": "#000000",
        "logo_background": "#002D72" 
      }
    },
    {
      "id": 102,
      "name": "Ашан",
      "logo_url": "https://cdn.petrushka.ru/logos/auchan.png",
      "target_url": "https://auchan.ru",
      "delivery_info": {
        "text": "Ближайшая доставка сегодня",
        "time_slot": "18:00-20:00",
        "is_express": false
      },
      "style": {
        "background_color": "#FFFFFF",
        "text_color": "#000000",
        "logo_background": "#FFFFFF"
      }
    },
    {
      "id": 103,
      "name": "ВкусВилл",
      "logo_url": "https://cdn.petrushka.ru/logos/vv.png",
      "target_url": "https://vkusvill.ru",
      "delivery_info": {
        "text": "Быстрая доставка",
        "time_slot": "от 20 до 60 минут",
        "is_express": true
      },
      "style": {
        "background_color": "#FFFFFF",
        "text_color": "#000000",
        "logo_background": "#FFFFFF"
      }
    },
    {
      "id": 104,
      "name": "ВИКТОРИЯ",
      "logo_url": "https://cdn.petrushka.ru/logos/victoria.png",
      "target_url": "https://victoria-group.ru",
      "delivery_info": {
        "text": "Ближайшая доставка сегодня",
        "time_slot": "17:00-19:00",
        "is_express": false
      },
      "style": {
        "background_color": "#FFFFFF",
        "text_color": "#000000",
        "logo_background": "#B8D432"
      }
    }
  ]
}
