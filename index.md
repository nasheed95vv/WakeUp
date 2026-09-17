# Политика конфиденциальности приложения WakeUp

Дата вступления в силу: 18.09.26

## Кратко

WakeUp не требует регистрации и не имеет собственного сервера — все
будильники, настройки и статистика хранятся только на вашем устройстве.
Приложение показывает рекламные баннеры (Yandex Mobile Ads SDK), поэтому
для их показа требуется подключение к интернету, и рекламная сеть Яндекса
может обрабатывать часть технических данных устройства — подробности
ниже.

## Какие данные собирает и хранит само приложение

WakeUp не собирает, не хранит на серверах и не передаёт третьим лицам:

- персональные данные (имя, номер телефона, email и т. д.);
- геолокацию;
- какие-либо файлы, контакты, фото или иной контент устройства;
- данные об использовании приложения (собственную аналитику).

## Реклама (Yandex Mobile Ads SDK)

Приложение показывает рекламные баннеры через Yandex Mobile Ads SDK
(рекламная сеть Яндекса). Для показа рекламы приложению требуется доступ
в интернет. Чтобы подобрать и показать рекламное объявление, SDK может
передавать рекламной сети такие данные, как:

- рекламный идентификатор устройства (Advertising ID);
- технические данные об устройстве (модель, версия ОС, язык, размер
  экрана и т. п.);
- приблизительное местоположение по IP-адресу.

Эти данные обрабатывает рекламная сеть Яндекса в соответствии со своей
политикой конфиденциальности: https://legal.yandex.ru/confidential/.
Само приложение WakeUp не хранит и не имеет доступа к этим данным — они
обрабатываются напрямую SDK и рекламной сетью.

Вы можете ограничить персонализацию рекламы или сбросить рекламный
идентификатор в настройках вашего устройства (обычно: Настройки → Google
→ Реклама, либо Настройки → Конфиденциальность → Реклама, в зависимости
от производителя устройства и версии Android).

## Что хранится локально на устройстве

Все данные, которые создаёт пользователь (будильники, их настройки,
статистика срабатываний, выбранная тема и градиент), хранятся **только**
в локальной базе данных и локальных настройках приложения на самом
устройстве. Эти данные удаляются при удалении приложения и никогда не
передаются на сервер WakeUp — потому что такого сервера просто нет.

Дополнительно все эти данные **зашифрованы прямо на диске** (AES-256):
база данных — через SQLCipher, настройки — значения по отдельности
шифруются ключом из защищённого хранилища. Ключ шифрования создаётся
случайным образом при первом запуске приложения и хранится только в
защищённом хранилище Android Keystore устройства (на большинстве
телефонов — в отдельном аппаратном модуле). Этот ключ никогда не встроен
в код приложения и не передаётся никуда — он уникален для каждой
установки на каждом устройстве. Поэтому даже при прямом доступе к файлам
приложения (root, adb, резервная копия) сами данные будут видны только
как нечитаемый шифротекст.

## Разрешения, которые запрашивает приложение, и зачем

| Разрешение | Зачем нужно |
|---|---|
| Точные будильники (`SCHEDULE_EXACT_ALARM` / `USE_EXACT_ALARM`) | Чтобы будильник срабатывал точно в выбранное время. |
| Уведомления (`POST_NOTIFICATIONS`) | Чтобы показать полноэкранный экран будильника и кнопку отключения в уведомлении. |
| Автозапуск при загрузке (`RECEIVE_BOOT_COMPLETED`) | Чтобы будильники продолжали работать после перезагрузки телефона. |
| Вибрация (`VIBRATE`) | Для вибросигнала будильника. |
| Фоновая служба (`FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MEDIA_PLAYBACK`) | Чтобы звук будильника продолжал звучать, даже если приложение свёрнуто. |
| Отключение блокировки экрана (`DISABLE_KEYGUARD`) / показ поверх экрана блокировки | Чтобы экран будильника был виден, даже если телефон заблокирован. |
| Интернет (`INTERNET`, `ACCESS_NETWORK_STATE`) | Чтобы запрашивать и показывать рекламные баннеры. |

Все разрешения, кроме двух последних, используются исключительно для
работы будильника на устройстве и не связаны со сбором данных.

## Дети

Приложение само по себе не собирает данные ни у кого, включая детей.
Однако, поскольку приложение показывает рекламу через стороннюю сеть, оно
не предназначено для детей младше 13 лет без надлежащего родительского
контроля за настройками рекламы устройства, если иное не установлено
возрастным рейтингом конкретного стора.

## Изменения политики

Если политика изменится, новая версия будет опубликована по этому же
адресу с обновлённой датой.

## Контакты

По вопросам, связанным с этой политикой, обращайтесь: [укажите ваш email]

---

# Privacy Policy — WakeUp (English)

Effective date: [set on publish]

## Summary

WakeUp requires no account and has no server of its own -- alarms,
settings, and statistics are stored only on your device. The app shows
advertising banners (Yandex Mobile Ads SDK), so it requires an internet
connection to display them, and the ad network may process some device
data to do so -- details below.

## Data the app itself collects and stores

WakeUp does not collect, store on any server, or share with third
parties: personal data, location, any files/contacts/photos on the
device, or its own usage analytics.

## Advertising (Yandex Mobile Ads SDK)

The app displays ad banners through the Yandex Mobile Ads SDK (Yandex
Advertising Network). Showing ads requires an internet connection. To
select and serve an ad, the SDK may share data such as:

- the device's advertising identifier;
- technical device data (model, OS version, language, screen size, etc.);
- an approximate location derived from IP address.

This data is processed by the Yandex Advertising Network under its own
privacy policy: https://yandex.com/legal/confidential/. WakeUp itself
does not store or have access to this data -- it is handled directly by
the SDK and the ad network.

You can limit ad personalization or reset your advertising identifier in
your device's settings (typically under Settings > Google > Ads, or
Settings > Privacy > Ads, depending on device maker and Android version).

## What is stored locally

Everything the user creates (alarms, their settings, trigger statistics,
chosen theme and gradient) is stored **only** in the app's local storage
on the device itself. This data is deleted when the app is uninstalled
and is never sent to a WakeUp server -- because no such server exists.

In addition, all of this data is **encrypted at rest** (AES-256): the
database via SQLCipher, the settings via values individually encrypted
with a key held in the Android Keystore. The encryption key is generated
randomly the first time the app runs and is kept only in the device's
Android Keystore (hardware-backed on most phones). This key is never
embedded in the app's code and never transmitted anywhere -- it is unique
to each install on each device. As a result, even with direct access to
the app's files (root access, adb, a backup), the raw data is unreadable
ciphertext.

## Permissions and why they're needed

| Permission | Why |
|---|---|
| Exact alarms (`SCHEDULE_EXACT_ALARM` / `USE_EXACT_ALARM`) | So the alarm fires exactly at the chosen time. |
| Notifications (`POST_NOTIFICATIONS`) | To show the full-screen alarm and the in-notification dismiss action. |
| Boot receiver (`RECEIVE_BOOT_COMPLETED`) | So alarms keep working after the phone restarts. |
| Vibration (`VIBRATE`) | For the alarm's vibration pattern. |
| Foreground service (`FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MEDIA_PLAYBACK`) | So the alarm sound keeps playing even if the app is backgrounded. |
| Show over lock screen / disable keyguard | So the alarm screen is visible even when the phone is locked. |
| Internet (`INTERNET`, `ACCESS_NETWORK_STATE`) | To request and display ad banners. |

All permissions except the last two are used solely for the alarm to work
on-device and are unrelated to data collection.

## Children

The app itself does not collect data from anyone, including children.
However, since the app shows ads through a third-party network, it is not
intended for children under 13 without appropriate parental control over
the device's ad settings, unless otherwise established by a specific
store's age rating.

## Changes

If this policy changes, an updated version with a new date will be posted
at the same URL.

## Contact

ra1111vvhh@gmail.com
