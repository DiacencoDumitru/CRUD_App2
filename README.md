## CRUD, Метод POST

### Теория:

* `@ModelAttribute` когда аннотирует метод (это означает что в каждую модель, в каждом методе текущего Controller'a мы
  хотим добавить какую-то пару ключ-значение).
* `@ModelAttribute` когда аннотирует аргумент метода (все эти 3 вещи ниже указанные берёт на себя ModelAttribute)
    1. Создание нового объекта
    2. Добавление значений в поля через сеттеры
    3. Добавление созданного объекта в модель

### Приложение:
* `@PostMapping` для изменения данных на сервере (допустим добавление нового человека в БД)
* `return "redirect:/people";` в Контроллере у метода create(), при создании человека будет нас перенаправлять на страницу списка людей.
* `person.setId(++PEOPLE_COUNT);` В PersonDAO в методе save(), у нас id должен быть уникальным и покамест мы будем id увеличивать самим, но обычно это делается с помощью БД автоматически, в дальнейшем мы это реализуем.
