1) Разобрать как работает вебсервер
2) Отличие встроенного сервера php от nginx apache
3) Разобрать почему во строенном сервере php не подгружаются картинки
4) Разобрать работу с куками и сессиями
5) ```php -s 0.0.0.0:8000 -t need_directory``` - запускает сервер
с указание рабочей папки
6) Проблемы публичных данных в куках

### Дома
...

1) Должна быть форма регистрации
username
password - не хранить в окрытом виде, исполузуй md5
role: {user, admin} - не регистрируют админа

name
age
phone
email

Данные сохранять не в сериализованном видео, а в json
serilize и unserilize меняем на json_edncode и json_decode 

При регистрации пользователю устанавливается роль user
Администратора нельзя через эту форму создать (кроме первого раза, как мы и договаривались)

Когда зарегестрировались, мы автоматом входим в систему

При заходе на эту страницу проверяем авторизован ли пользователь, если в сессии есть пользователь, то редиректим на profile


2) Форма авторизации
username
password

Мы проверяем, что пользователь авторизован и редиректим
на страницу profile

3) profile
Показываем всю информацию пользователя

------ Админские страницы -----

4) Страница списка пользователей (users)

Если на эту страниу перейдет не авторизованный пользователь, то
редиректим на 404 страницу

Если пользователь авторизован, но роль у него user, редиректим 
на 404

Если роль admin то все отображаем

5) Страница добавления пользователя
Роль можно задать (user|admin)
Грубо говоря, похожа полями на страницу регистрации, добавляется поле выбора роли

6) Страница редактирования пользователя

7) Удаление пользователя


-- Статистика, работа с куками и только с ними=), почти только
с ними)))) Это на потом