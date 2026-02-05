<img width="922" height="230" alt="изображение" src="https://github.com/user-attachments/assets/43a1d55c-cf13-4baa-af05-e513d6522861" />

# Список инструкций для настройки RouterOS

+ **RussianIP** - список всех сетей и масок, принадлежащих РФ. Создаётся address list  и добавляется правило в RAW , по запрету доступа к L2TP, НЕ из диапазона address list RussianIP, до обработки firewall, для снижения нагрузки на железо. При желании, можно изменить протокол, на свой. 

+ **BlockWinboxWAN** - 3в1: правило в firewall/filter, RAW и script. Создаёт правило в firewall/fiter о добавлении ip-адресов, кто ломится на порт 8291(порт winbox), за исключением белого списка. Далее правило в RAW, где идёт блокирока всех ip-адресов address list, до обработки firewall, для снижения нагрузки на роутер. Дополнительно скрипт от админа, по поиску фразы "denied winbox/dude connect from" и добавление ip-адреса в address list. Также создаётся правило в планировщике, на ежедневный запуск скрипта в 06:01 утра.
> [!CAUTION]
> **ОБЯЗАТЕЛЬНО ИЗМЕНИТЬ ИМЯ ПОЛЬЗООВАТЕЛЯ В СКРИПТЕ НА СВОЕГО  !!!**


# Example headings

## Sample Section

## This'll be a _Helpful_ Section About the Greek Letter Θ!
A heading containing characters not allowed in fragments, UTF-8 characters, two consecutive spaces between the first and second words, and formatting.

## This heading is not unique in the file

TEXT 1

## This heading is not unique in the file

TEXT 2

# Links to the example headings above

Link to the sample section: [Link Text](#sample-section).

Link to the helpful section: [Link Text](#thisll-be-a-helpful-section-about-the-greek-letter-Θ).

Link to the first non-unique section: [Link Text](#this-heading-is-not-unique-in-the-file).

Link to the second non-unique section: [Link Text](#this-heading-is-not-unique-in-the-file-1).
