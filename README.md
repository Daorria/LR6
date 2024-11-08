# Лабораторная работа №6
**Цель работы:** изучние базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

**Работу выполнила:** Иваненко Дарья Игоревна гр.4315
## Создание аккаунта в Github
До выолнения лабораторной работы был создан аккаунт Daorria.

![Akk](https://github.com/Daorria/LR6/blob/report/image/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20234533.png)
## Установка Git
До выполнения лабораторной работы был установлен Git.

![Yst](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20234633.png)

## Настройка клиента Git
Указываем ФИО и номер группы в никнейме и свою почту.

```
git config --global user.name "Ivanenko Darya Igorevna 4315"
git config --global user.email "ivanenkolgaigor@gmail.com"
```


![nastroika](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223053.png)

## Клонирование репозитория
Создаем копию [репозитория](https://github.com/Kurtyanik/LR6), нажав fork.
![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20222755.png)
После создания fork, появятся все файлы репозиторя, над которыми можно проводить различные действия (удаление, добавление, изменение), не меняя при этом репозиторий автора.

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20222825.png)

## Клонирование личного удалённого репозитория на компьютер
Создаем клон репозитория на свой компьютер с помощью команды:

```
git clone https://github.com/Daorria/LR6
```

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223140.png)

## Добавление файла через интерфейс GitHub
В репозитории создаем новый файл, нажав **Add file** >> **Create new file**.

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223201.png)

Необходимо придумать название файла и то, что в нем будет находится. Далее, нажимаем на кнопку Commit changes и добавляем сообщение.
![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223240.png)

Файл forLab6 будет отображаться в удаленном репозитории.

Переходим в папку LR6, используя команду:

```
cd LR6
```

Подтягиваем изменения с удалённого репозитория в локальный, воспользовавшись командой:

```
git pull
```

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223320.png)

В папке LR6 появился файл forLab6.

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223344.png

## Вывод историй операций
Для того, чтобы посмотреть историю операций для каждой из веток, используем команду:

```
git log --all
```
![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223433.png)

## Просмотр последнего изменения
Просмотр последнего изменения осуществляется с помощью команды:

```
git log -p -1
```

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223457.png)

## Слияние. Конфликт и его разрешение

Попытаемся осуществить слияние веток master и branch1, используя команду:

```
git merge origin/branch1
```

Возникнет конфликт так как файл с одним названием содержит разную информацию.

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223537.png)

Чтобы разрешить конфликт, необходимо открыть mergefile.txt в любом редакторе и прининять изменения только от HEAD.

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223600.png)

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223617.png)

Добавляем уже измененный файл, используя команду:

```
git add mergefile.txt
```
Делаем коммит:

```
git commit -m"Изменение файла mergefile".
```

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223747.png)

Теперь,слияние веток будет успешным.

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20223828.png)

## Удаление побочной ветки
Для того, чтобы удалить ветку branch1 в локальном репозитории, необходимо воспользоваться командой:

```
git branch -d branch1
```

Чтобы добавить изменения в удаленный репозиторий, воспользуемся командой:

```
git push origin --delete branch1
```

чтобы посмотреть,удалилась ли ветка, используем команду:
```
git branch
```

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20224828.png)

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20224853.png)

## Откат коммитов
Добавим три файла, сделав 3 коммита, используя следующие команды:

```
git add file1.txt
git commit-m"Первый коммит"
git add file2.txt
git commit -m"Второй коммит"
git add file3.txt
git commit -m"Третий коммит"
git push
```
![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20230710.png)

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20230833.png)

Проверяем наличие файлов с коммитами в удаленном репозитори и в локальном.

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20230848.png)

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20230958.png)

Для отката до предыдущего коммита, воспользуемся командой:

```
git reset --hard HEAD~1
```

![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20231713.png)

Добавляем откат коммита в удаленный репозиторий, воспользовавшись командой:

```
git push -f origin master
```
![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20231836.png)


![](https://github.com/Daorria/LR6/blob/report/images/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202024-11-07%20231852.png)


