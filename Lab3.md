**Lab 3**
Нашей задачей было написать такой скрипт, чтобы при его пуше в гитхаб автоматически собирался докер образ и результат сборки сохранялся. Мы написали докер файл, в котором в текстовый файл записывалась некоторая информация. Теперь пройдем по шагам.
1. Создаем отдельный репозиторий (вот этот)), загружаем сюда нужные файлы (Dockerfile), создаем директорию .github/workflows. Используем github actions. Также код Докер файла можно увидеть на картинке ниже.
<img width="308" alt="Снимок экрана 2023-12-03 в 13 43 14" src="https://github.com/mariabakhareva/lab3/assets/112972915/da1cdd2c-f31b-4f5e-9b62-781eea71ef64">

<img width="1140" alt="Снимок экрана 2023-12-03 в 13 30 19" src="https://github.com/mariabakhareva/lab3/assets/112972915/810d09c1-98bd-4964-80d0-00970dcb73cf">

2. Затем добавляем секреты в реп, они хранят имя пользователя и пароль от его DockerHub.
<img width="788" alt="Снимок экрана 2023-12-03 в 13 29 58" src="https://github.com/mariabakhareva/lab3/assets/112972915/5b142123-d57c-4d88-b89b-6b7875755059">
3. Создаем файл docker-push.yml в директории .github/workflows. Его код можно увидеть на представленной ниже картинке. В нем последовательно расписаны шаги выполнения скрипта: сменяем директорию на эту, осуществляем вход по заранее подготовленным секретам - имени пользователя и паролю в Docker Hub, затем собирается и пушится образ.
<img width="1148" alt="Снимок экрана 2023-12-03 в 13 30 11" src="https://github.com/mariabakhareva/lab3/assets/112972915/54de0e85-b7c2-489d-a51e-46c44439b714">

4. Пушим в Github, у нас сразу появляется Workfkow и успешная реализация скрипта. Проверяем на самом сайте Docker Hub - образ появился.
<img width="637" alt="Снимок экрана 2023-12-03 в 23 07 28" src="https://github.com/mariabakhareva/lab3/assets/112972915/9668587d-1332-4c77-aebd-0a02fb534b79">
<img width="652" alt="Снимок экрана 2023-12-03 в 23 10 25" src="https://github.com/mariabakhareva/lab3/assets/112972915/3602c507-6df1-4515-af7d-370451afe74d">



