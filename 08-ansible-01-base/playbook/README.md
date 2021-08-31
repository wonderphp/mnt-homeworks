# Самоконтроль выполненения задания

1. Где расположен файл с `some_fact` из второго пункта задания?  
   group_vars/all/examp.yml  
   
2. Какая команда нужна для запуска вашего `playbook` на окружении `test.yml`?  
   ansible-playbook -i inventory/prod.yml site.yml --vault-pass "key"  
   
3. Какой командой можно зашифровать файл?  
   ansible-vault create <filename>  
   
4. Какой командой можно расшифровать файл?  
   ansible-vault decrypt <filename>  
   
5. Можно ли посмотреть содержимое зашифрованного файла без команды расшифровки файла? Если можно, то как?  
    ansible-vault view <filename>  
   
6. Как выглядит команда запуска `playbook`, если переменные зашифрованы?  
   через файл с ключом: ansible-playbook -i inventory/prod.yml site.yml --vault-pass "key"
    или  из строки ansible-playbook -i inventory/prod.yml site.yml --ask-vault-pass для ваулт --ask-pass для ССШ
7. Как называется модуль подключения к host на windows?  
   winrm
   
8. Приведите полный текст команды для поиска информации в документации ansible для модуля подключений ssh  
   ansible-doc -t connection ssh  
   
9. Какой параметр из модуля подключения `ssh` необходим для того, чтобы определить пользователя, под которым необходимо совершать подключение?  
         
   remote_user
           User name with which to login to the remote server, normally set by the remote_user keyword.
           If no user is supplied, Ansible will let the ssh client binary choose the user as it normally
             - key: remote_user