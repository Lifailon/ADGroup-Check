## AD-Group-Check - мониторинг членства в группе AD.

Вначале скрипт проверяет наличие txt-файла с именем группы (в директории %userprofile%\Documents), который содержит список членов в группе, и использует его, как эталонный, для сопоставления с текущим членством, если файл отсутствует, то создает его (в дальнейшем, что бы зафиксировать актуальные изменения в группе, достаточно удалить этот файл, можно автоматизировать данный процесс, но нужно добавить логирование изменений в новый файл, т.к. оповещение может затеряться). Если были внесены изменения в группу (имя группы меняется в первой строке скрипта), то фиксируется количество измененных объектов в большую или меньшную сторону и список пользователей, который был добавлен или исключен. Скрипт отправляет оповещение на почту (изменить 2-4 строки и раскомментировать 31-33, авторизация не используется) и уведомление Windows пользователю в текущей сессии.

![Image alt](https://github.com/Lifailon/AD-Group-Check/blob/rsa/WinNotify.jpg)
