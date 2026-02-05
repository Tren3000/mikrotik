<img width="922" height="230" alt="изображение" src="https://github.com/user-attachments/assets/43a1d55c-cf13-4baa-af05-e513d6522861" />

# Список инструкций для настройки RouterOS

+ $\color{green}{RussianIP}$ - список всех сетей и масок, принадлежащих РФ. Создаётся address list  и добавляется правило в RAW , по запрету доступа к L2TP, НЕ из диапазона address list RussianIP, до обработки firewall, для снижения нагрузки на железо. При желании, можно изменить протокол, на свой. 

+ $\color{green}{BlockWinboxWAN}$ - 3в1: правило в firewall/filter, RAW и script. Создаёт правило в firewall/fiter о добавлении ip-адресов, кто ломится на порт 8291(порт winbox), за исключением белого списка. Далее правило в RAW, где идёт блокирока всех ip-адресов address list, до обработки firewall, для снижения нагрузки на роутер. Дополнительно скрипт от админа, по поиску фразы "denied winbox/dude connect from" и добавление ip-адреса в address list. Также создаётся правило в планировщике, на ежедневный запуск скрипта в 06:01 утра.
> [!CAUTION]
> **ОБЯЗАТЕЛЬНО ИЗМЕНИТЬ ИМЯ ПОЛЬЗООВАТЕЛЯ В СКРИПТЕ НА СВОЕГО  !!!**

The background color is `#ffffff` for light mode and `#000000` for dark mode.
