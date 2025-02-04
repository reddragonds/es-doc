# Распостранённые ошибки и пути их решения

На данной странице используются сокращения:

- **Q** (question) - вопрос
- **A** (answer) - ответ

[[toc]]

## _Загрузил мод в стим, а он выдаёт Traceback. Мод в папке `mods`_.

**Q**: Я загрузил мод в стим, который до этого редактировался и всячески видоизменялся в папке `mods`. Загрузил, основной папкой указал `mods`. После загрузки версии мода из стима и захода в игру — выдаёт трейсбек.

**A**: У вас ошибка в путях к моду при загрузке оного в стим. Если мод и пути файлов для мода проходят через папку `mods`, то необходимо сделать следующее:

1. Создать отдельную папку с любым именем. Например, `my_mod_folder`
2. Внутрь неё засунуть папку `mods` вместе с папкой своего мода. Теперь путь к папке мода предположительно таков — `my_mod_folder/mods/my_mod/`
3. Снова переходим в загрузчик модов, открываем. Либо удаляем предыдущую версию мода и начинаем заново, либо нажимаем `Обновить существующий мод в мастерской`.
4. Основной папкой мода при загрузке указываем `my_mod_folder`, а не `mods` или `my_mod`.
5. Загружаем мод, перепроверяем подпиской и запуском версии мода из мастерской.

::: tip
Не забудьте переместить куда-нибудь вашу версию мода, с которой вы ранее работали, ибо если внутри БЛ будет и основная версия, и версия мода из мастерской — вылетит трейсбек из-за дублирования лейблов и папок.
:::

## _Ren'Py не находит изображение/видеофайл/аудиофайл. Пути сто раз перепроверены_.

**Q**: Пользуясь ручным объявлением видеофайла/аудиофайла/изображения я столкнулся с проблемой — при показе/воспроизведении файла, Ren'Py выдаёт трейсбек, указывая, что файл не найден. Пути в объявлении проверены.

**A**: Как бы смешно это не звучало, но советуем ещё раз перепроверить путь. Поискать ошибки в написании расширении файла, а также поискать лже-буквы (скажем, одна буква, написанная кириллицей внутри слова, написанного латиницей). В крайнем случае — проверьте файл на "битость". Если файл оказался "битым", то Ren'Py его "не увидит".

## _Не понимаю как загрузить мод из любой директории!_

**Q**: Переместил папку с модификацией на рабочий стол. Поработал над кодом, добавил пару файлов. После загрузки мода в стим и скачки его из мастерской — вылетает трейсбек. Указывает на ошибку в путях к файлам.

**A**: Для того, чтобы загрузить модификацию из любой директории, вам необходимо проделать следующее:

1. Создать папку с любым именем. Например, `my_mod_111`.
2. Внутрь неё переместить папку с вашей модификацией (например, `my_mod_root`). Теперь путь к файлам вашей модификации будет примерно таков — `my_mod_111/my_mod_root/`

::: tip
Если папка с модификацией лежит на рабочем столе, то путь будет следующим — `C:/Users/UserName/Desktop/my_mod_111/my_mod_root/`, где:

- `UserName` — имя пользователя вашей ОС

- `C:` — метка основного диска, на котором лежит ваша ОС. По умолчанию — `C:`

:::

3. Открыть загрузчик модов и обновить существующий мод (или загрузить его заново), указав основной папкой мода `my_mod_111`.
4. Загрузить мод, проверить на наличие ошибок в версии мода из мастерской.

::: tip
Не забудьте переместить куда-нибудь вашу версию мода, с которой вы ранее работали, ибо если внутри БЛ будет и основная версия, и версия мода из мастерской — вылетит трейсбек из-за дублирования лейблов и папок.
:::
