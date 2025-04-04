**Работает с версией API v2**

---

#### Установка переменных в `dump_to_json.py`

- `mgmt_ip`         — IP-адрес системы управления MGMT.
- `mgmt_login`      — Логин.
- `mgmt_pass`       — Пароль.
- `groupe_name`     — Имя группы.
- `precedence`      — Приоритет pre/post
- `path_save_json`  — Путь до папки для сохранения JSON (папку необходимо создать заранее).
- `path_save_html`  — Путь до папки для сохранения HTML (папку необходимо создать заранее).

---

#### Формирование HTML

- `to_html_groups_ip.py`         — Состав группы адресов.
- `to_html_groups_service.py`    — Состав группы сервисов.
- `to_html_rules.py`             — Правила безопасности.
- `find_ip_in_rule.py`           — Вхождение IP в правила безопасности, NAT, группы. Ищет только в рамках одной группы. Если правило в группе Global а IP в другой, то результат будет пустой.

**Необходимо указать путь до папки, куда выгрузили JSON, и путь до папки, куда сохранится HTML:**

```python
folder_path_json = "C:/Users/sb/json/"
folder_path_html = "C:/Users/sb/html/"
```

В `to_html_rules.py` можно задавать выходной файл черно-белый или цветной (`color=False`). Цветами выделены разные типы объектов. Легенда с цветами находится в самом низу таблицы:

```python
main(patch_to_json, path_to_html, color=True)
```

---
Пример вывода в папке [html](https://github.com/Srg-Blmv/pt-Rules-to-HTML/tree/main/html)


