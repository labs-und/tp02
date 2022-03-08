# LABORATORY WORK 2
## PART1

Создание файла .cpp

![image](https://user-images.githubusercontent.com/87879854/157311495-d3199939-222b-40f4-b9df-5040ffdb9b56.png)

```
git add hello_world.cpp
git commit -m "add hello world"
```

![image](https://user-images.githubusercontent.com/87879854/157312336-9bd973c8-d2ad-479b-9708-f4eda1c1c93a.png)

```
git add hello_world.cpp
git commit -m "hello world v 2.0"
git push origin master
```

## PART2

![image](https://user-images.githubusercontent.com/87879854/157313598-b4d902f6-f124-4937-bba5-1ba32ed2f44d.png)

```
git checkout -b patch1
git add hello_world.cpp
git commit -m "del using namespace"
git push origin patch1
```

Создание пул-реквества

![image](https://user-images.githubusercontent.com/87879854/157321186-f326c12b-4f27-4ead-b5c9-9e1739b734eb.png)

Добавление комментариев в код 

![image](https://user-images.githubusercontent.com/87879854/157321321-49e13b0d-96ae-4155-bf84-50c1ee0c8be1.png)

```
git add hello_world.cpp
git commit -m "comms added"

```

![image](https://user-images.githubusercontent.com/87879854/157333813-e245867e-ff16-4659-aa39-ae6db77978f2.png)

Выполняем слияние PR и удаление ветки patch1
```
git pull origin
```

![image](https://user-images.githubusercontent.com/87879854/157334406-6a2b5414-492f-4498-9be0-a200c3e3b9ab.png)

Локальное удаление ветки `git branch -D patch1`

## PART3

`git checkot -b patch2` Создание новой ветки

`clang-format --style="{BasedOnStyle: Mozilla}" hello_world.cpp` Форматирование файла .cpp

![image](https://user-images.githubusercontent.com/87879854/157337718-7741761b-f037-4fa4-98ff-5d93a06287be.png)

```
git add hello_world.cpp
git commit -m "clang"
git push origin patch2
```
После этого создаем PR из patch2 в master
Появились конфликты 

![image](https://user-images.githubusercontent.com/87879854/157338305-6be6ce92-8c7e-4cca-b240-16fcf8859b06.png)

```
git pull origin master
git rebase master  (появились ошибки)
cat hello_world.cpp
(ручная правка)
git rebase --continue
git push -f origin patch2
```
Конфликт исчез 

![image](https://user-images.githubusercontent.com/87879854/157345382-b50c229c-ca0f-4e26-96a2-224583060c32.png)

Мерж осуществлён 

![image](https://user-images.githubusercontent.com/87879854/157345478-c790e4d9-50dc-411a-983f-5f087aa3baf4.png)


