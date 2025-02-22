Лабораторная работа
Задание 1
Парамонов К-ИСП 39-1 

Установили Oracle linux
![image](https://github.com/user-attachments/assets/244a15d8-2a4d-49ba-978a-0b4dac0069dc)

Установили гостевые дополнения по инструкции: 
[инструкция для VBoxGA.docx](https://github.com/user-attachments/files/18921020/VBoxGA.docx)

После выполнения команды 
`sudo yum install wget` 
Возникла ошибка, указывающая на отсутствие прав доступа (`is not in the sudoers file`).  Для решения проблемы необходимо войти в систему от имени суперпользователя с помощью команды `su`.
![image](https://github.com/user-attachments/assets/4a6df09a-9526-4368-8188-55702ef3aac6)

Этот промах указывает путь к команде 
`sudo vi /etc/sudoers`
которая генерирует конфигурационный файл.  В него добавлена строка `Larin ALL=(ALL) ALL` (проблемы могут возникнуть из-за необходимости нажатия Tab).  Для сохранения изменений и выхода из файла нужно нажать Shift + : и выполнить команду 
`wq!`.
![image](https://github.com/user-attachments/assets/18725e7a-5821-4e3b-9493-edbf1fe1f580)

![image](https://github.com/user-attachments/assets/11723064-3289-4039-925e-0ef8f7a5799b)

После всех этих операций снова вводим команду:
`sudo yum install wget`
А затем, чтобы проверить успешность загрузки, используем команду:
`wget --version`.
