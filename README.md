# Небольшой учебный проект, в котором я разрабатываю API.

### Описание
Это учебный проект по разработке API, позваляющий работать с  темами, постами и их комментариями.
В дальнейшем данный проект будет использован с проектом на React. Ссылка: [Git](https://github.com/BolotnikovMS/test-task-react).

### Возможности
Данное API позволяет следующие возможности:
- Регистрация и авторизация по токену;
- Созданиею/получение тематик для постов;
  - Получение постов по определенной теме;
- Созданиею/Получение поста определенной темы;
  - Получение комментариев к определенному посту;
- Созданиею/получение всех комментария;
- Использование параметров(сортировка, разбите на страницы и т.д.);

### Работа с проектом
Для работы с проектом необходимо выполнить следующие действия:
1. Скопировать проект удобным способом.
2. Установить зависимости.

```
npm install
```
3. Скопировать файл .env.example  и переименовать его в .env
4. Выполнить миграцию таблиц базы данных.
```
node ace migration:run
```
5. Запустить сервер. 
```
npm run dev
```
Сервер будет запущен на порту 3333. http://127.0.0.1:3333

6. Для удобства можно сгенерировать фейковые данные. Для этого необходимо перейти по следующим url:  
Для генерации тем: http://127.0.0.1:3333/api/v1/faker/topics  
Для генерации постов: http://127.0.0.1:3333/api/v1/faker/posts  
Для генерации комментариев: http://127.0.0.1:3333/api/v1/faker/comments
7. Для выполнения запросов необходимо создать пользователя и использовать token при выполнении запросов.  
Для этого необходимо выполнить post запрос с данными для регистрации пользователя по url: http://127.0.0.1:3333/api/v1/register  
Далее http://127.0.0.1:3333/api/v1/login после чего в ответе будет token.

### Прогресс
- [✅] Схемы бд.
- [✅] Модели для работы с бд: Topic, Post, Comment, User.
- [✅] Роутинг.
- [✅] Авторизация по токену.
- Контроллеры для работы с логикой:
  - TopicsController 
    - [✅] Получение всех тем;
    - [✅] Получение определенной темы;
    - [✅] Получение постов по определнной теме;
    - [✅] Добавление новой темы;
    - [✅] Изменение определенной темы;
    - [✅] Удаление темы;
  - PostsController
    - [✅] Получение всех постов;
    - [✅] Получение определенного поста;
    - [✅] Получение комментариев к определенному посту;
    - [✅] Добавление нового поста;
    - [✅] Изменение поста;
    - [✅] Удаление поста;
  - CommentsController
    - [✅] Получение всех комментариев;
    - [✅] Добавление нового комментария;
    - [✅] Изменение комментария;
    - [✅] Удаление комментария;
- Схемы валидации данных при добавлении
  - [] Тем;
  - [] Постов;
  - [] Комментариев;
  - [] Регистраций;
