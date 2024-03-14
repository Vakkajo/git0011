
## Задания

1. Создал учетную запись на GitHub.
      ```
      git config --global user.name "Vakkajo"
      git config --global user.email "nikitayn433@mail.ru"
      ```
2. Создал папку для работы с Git:
      ```
      mkdir git_00
      ```
3. Создал репозиторий на GitHub:
   * Создал локальный репозиторий:
   
      ```
      git init
      ```
4. Добавил пустой текстовый документ:
    ```
    echo > TEST.txt
    ```
	```
    git add TEST.txt
    ```
5. Добавил commit для каждого абзаца:
    ```
    git commit -m "Комментарий"
    ```
    ![](/imgGit/001.png)
6. Просмотрел статус текущего репозитория:
    ```
    git status
    ```
    ![](/imgGit/002.png)
7. Добавил еще один файл:
    ```
    echo > TEST2.txt
    ```
	```
    git add TEST2.txt
    ```
8. Создал коммит:
    ```
    git commit -m "Комментарий"
    ```
    ![](/imgGit/003.png)
9. Посмотрел протокол коммитов:
    ```
    git log
    ```
    ![](/imgGit/004.png)
10. Посмотрел изменения в файле по сравнению с последним коммитом:
    ```
    git diff
    ```
11. Убрал изменения относительно последнего коммита из файла:
    ```
    git checkout -- TEST.txt
    ```
12. Посмотрел существующие ветки:
    ```
    git branch
    ```
    ![](/imgGit/005.png)
13. Создал новую ветку:
    ```
    git branch new
    ```
14. Переключился на новую ветку:
    ```
    git checkout new
    ```
    ![](/imgGit/006.png)
15. Создал новую ветку и сразу же переключилися на нее:
    ```
    git checkout -b new2
    ```
16. Удалил ветку:
    ```
    git branch -d new
    ```
    ![](/imgGit/007.png)
17. Добавил merge изменения из указанной ветки в текущую:
    ```
    git checkout new2
    git merge master
    ```
18. Создал конфликт:
    ```
    git checkout master
    ```
      ```
      git add TEST.txt
      git commit -m "Changes"
      ```
      ![](/imgGit/008.png)
    
      ```
      git add TEST.txt
      git commit -m "Changes"
      ```
      ![](/imgGit/009.png)
      
      ```
      git checkout master
      git merge new2
      ```
      ![](/imgGit/010.png)
19. Посмотрел в каких файлах есть конфликты:
    ```
    git status
    ```
    ![](/imgGit/011.png)
20. Устранил конфликт:
      ```
      git add TEST.txt
      git commit -m "Resolved conflict"
      ```
      ![](/imgGit/012.png)
21. Переключился на указанный коммит:
    ```
    git checkout eea2578
    ```
    ![](/imgGit/013.png)
22. Сделал ребазирование текущей ветки:
    ```
    git rebase master
    ```
23. Удалил ветку:
    ```
    git branch -d new2
    ```
24. Пропустил текущий конфликтный коммит и перешел к следующему:
    ```
    git rebase --skip
    ```
25. Отправил изменения из локального репозитория для указанной ветки в удаленный (дистанционный):
    ```
    git remote add origin https://github.com/Vakkajo/git0011.git
    git push origin master
    ```
    ![](/imgGit/014.png)
26. Забрал изменения из репозитория, для которого были созданы удаленные ветки по умолчанию:
    ```
    git pull origin master
    ```
    ![](/imgGit/015.png)
27. Забрал изменения удаленной ветки из репозитория основной ветки по умолчанию:
    ```
    git checkout -b new3
    echo > TEST3.txt
    git add TEST3.txt
    git commit -m "New3"
    git push origin new3
    git pull origin new3:master
    ```
    ![](/imgGit/016.png)
28. Клонировал репозиторий:
    ```
    git clone https://github.com/Vakkajo/git0011.git
    ```
    ![](/imgGit/017.png)
