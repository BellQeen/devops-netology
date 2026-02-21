# devops-netology
Study tasks for DevOps cource from Netology.

В репозиторий terraform не будут попадать:
- .terraform/  
Вся папка .terraform целиком, включая все файлы и вложенные каталоги внутри неё
- \*.tfstate  
Все файлы с расширением .tfstate
- \*.tfstate.\*  
Все файлы, имя которых начинается с любого набора символов, затем .tfstate., а после него — любое продолжение
- Файл crash.log 
- crash.*.log  
Все файлы, которые начинаются с crash., затем содержат любую последовательность символов и заканчиваются на .log
- *.tfvars  
Все файлы с расширением .tfvars
- *.tfvars.json  
Все файлы, которые заканчиваются на .tfvars.json
- Файл override.tf
- Файл override.tf.json
- *_override.tf  
Любой файл, который заканчивается на _override.tf
- *_override.tf.json  
Любой файл, который заканчивается на _override.tf.json
- Файл .terraform.tfstate.lock.info
- Файл .terraformrc
- Файл terraform.rc