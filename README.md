# deblinux
При, крч, тут мои дебиановские посиделки


## с чего бы начать...
Выбор любого дистрибутива начинается с осознания своих потребностей. После этого идет переход к выбору софта... И в этом плане побеждает Арч со своим АУРом, где валяется больше пакетов, чем может вместиться глистов в Обаму. 
И казалось бы... победил Арч по своей универсальности, но не тут-то было. В игру вступает Генту, где можно не ставить системД, есть ГУРУ(аналог аура), так еще весь софт (в особенности ядра) компилируешь под СВОИ задачи. Но тут раз и сложность. А сложность в том, что слишком сложно. И оба этих дистрибутива имеют модель ролинг-релизов, то бишь пока не обновишься - все стабильно. Но мейнтейнером системы выступает сам пользователь, и это проблема. Есть еще такая штука как Федора, у которой все всегда хорошо, но упс... это не то, если строишь свою систему с нуля, то будь добр в Федора Еврисинг сначала не забудь поставить дрова на интернет без интернета. ОпенСУЗИ позволяет галочками выбрать софт, который тебе нужен, но там настолько далеко отошли от КИСС, что ПерекатиПОЛЕ - это лучшее название для дистрибутива, куда пакеты попадают быстрее, чем в экстра Арча, но при этом никто не хочет поработать с зависимостями. Чемпион по количеству минимальных зависимостей - ВОИД. Но у Воида свои заморочки из-за избегания СистемД, сюда же идет и Артикс, у которого точно такая же проблема. Дальше - больше, у нас есть такой феномен Immutable дистрибутивов, где у нас такая классная система слоев пакетов, что ты не можешь поставить какой-нибудь хайпрленд без китти, но дает приемущество, что обновления хоть и занимают несколько часов(привет выше упомянутый генту), ты всегда сможешь загрузить на рабочую машинку.
ЧЕСТНО. я вижу будущее за Immutable форматом дистрибутивов. И вижу все приемущества софта именно на АРЧе. Но раз за разом... ставя Арч я возвращаюсь на обычную федору, потому что все работает, а дрова ставятся, как по волшебству.


## Репозитории Трикси
На данный момент стабильной версией дебиана является Букворм, но по сути - правило "реже обновления - больше стабильности" работает на всех дистрибутивах. Поэтому немного увеличим количество софта, установив не совсем стабильные пакеты...
## Дрова на дебиане
По люто непонятным причинам, я не знал, что нвидиа держат репозиторий для дебиана(как для тамблвида). А ставится все в пару строчек... И все было написано на ВИКИ ДЕБИАНА!!!
![image](https://github.com/user-attachments/assets/c02dd3ce-da90-48f7-bd15-78b79a7b35f9)
коротко о том, что здесь написано: у нас есть [репозитории](https://developer.download.nvidia.com/compute/cuda/repos), которые можно поставить, если прочитать [мануал](https://docs.nvidia.com/datacenter/tesla/driver-installation-guide).
Мы юзаем Дебиан 12(который Букворм, но с разными репами, в том числе трикси, но пока что именно дебиан 12), и вот такие строчки у нас:
```
apt install linux-headers-$(uname -r)
apt install software-properties-common wget
add-apt-repository contrib
wget https://developer.download.nvidia.com/compute/cuda/repos/debian12/x86_64/cuda-keyring_1.1-1_all.deb
dpkg -i cuda-keyring_1.1-1_all.deb
apt update
apt install nvidia-driver
```
## Список софта, который нужен мне
```
fastfetch
nmcli
nautilus
hyprland
kitty
waybar
swayosd
swaync
chromium
pipewire
pavucontrol
neovim
и хоть какой-нибудь лаунер приложений
```


