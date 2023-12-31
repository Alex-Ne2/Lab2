# Lab2
Homework
Part I
1. Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com).

2. Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге. ![image]( ![image]( ![image]( ![image](

get init - создание пустого локального репозитория
git remote add origin ... - добавление удаленного репозитория и присвоение ему названия
git pull origin main - синхронизация с удалённым репозиторием\

3. Создайте файл hello_world.cpp в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу Hello world на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку `using namespace std

4. Добавьте этот файл в локальную копию репозитория.

5. Закоммитьте изменения с осмысленным сообщением. ![image]( ![image]( ![image]( git status - просмотр текущих изменений
git add - добавить файл в локальный репозиторий
git config --global user.email - настройка адреса электронной почты
git commit -m - описание коммита в локальном репозитории
git push - отправка изменений в удалённый репозиторий\

6. Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение Hello world from @name, где @name имя пользователя.

7. Закоммитьте новую версию программы. Почему не надо добавлять файл повторно git add? ![image]( git commit -a -m - добавление файла в локальный репозиторий и закоммитирование его\

8. Запуште изменения в удалёный репозиторий. ![image](

9. Проверьте, что история коммитов доступна в удалёный репозитории. ![image](

git log - просмотр истории изменений



Part II



Note: Работать продолжайте с теми же репоззиториями, что и в первой части задания.

1. В локальной копии репозитория создайте локальную ветку patch1.
![image](

git checkout -b - переключение ветвей

2. Внесите изменения в ветке patch1 по исправлению кода и избавления от using namespace std.

3. commit, push локальную ветку в удалённый репозиторий. ![image](

4. Проверьте, что ветка patch1 доступна в удалёный репозитории.

5. Создайте pull-request patch1 -> master. ![image](

6. В локальной копии в ветке patch1 добавьте в исходный код комментарии. ![image](

7. commit, push. ![image]( ![image](

8. Проверьте, что новые изменения есть в созданном на шаге 5 pull-request ![image](

9. В удалённый репозитории выполните слияние PR patch1 -> master и удалите ветку patch1 в удаленном репозитории.

10. Локально выполните pull.

![image](

11. С помощью команды git log просмотрите историю в локальной версии ветки master.
![image](

12. Удалите локальную ветку patch1.
![image](

git branch -d - удаление ветки\



Part III



Note: Работать продолжайте с теми же репоззиториями, что и в первой части задания.

1. Создайте новую локальную ветку patch2.
2. Измените code style с помощью утилиты clang-format. Например, используя опцию -style=Mozilla.
![image](

style= - загрузка конфигурации стиля
clang-format -i - форматирование файла на место\

3. commit, push, создайте pull-request patch2 -> master.
![image](

4. В ветке master в удаленном репозитории измените комментарии, например, расставьте знаки препинания, переведите комментарии на другой язык.

5. Убедитесь, что в pull-request появились конфликтны.

![image](

6. Для этого локально выполните pull + rebase (точную последовательность команд, следует узнать самостоятельно). Исправьте конфликты. Нажал на исправление конфликт и убрал ошибки\

7. Сделайте force push в ветку patch2

![image](

git push -f удаляет из ветки на сервере все коммиты, которых нет в локальной версии, и записывает новые
8. Убедитеcь, что в pull-request пропали конфликтны.

9. Вмержите pull-request patch2 -> master.
