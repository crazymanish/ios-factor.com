Исторически существуют значительные различия между разработкой (разработчик делает живые изменения на локальном развёртывании приложения) и работой приложения (развёртывание приложения в App Store с доступом к нему конечных пользователей). Эти различия проявляются в трёх областях:

- **Различие во времени:** Разработчик может работать с кодом, который попадёт в рабочую версию приложения только через дни, недели или даже месяцы.
- **Различие персонала:** Все разработчики iOS пишут код, только один человек знает, как развернуть приложение
- **Разрыв в инструментах:** Разработчики могут использовать промежуточный сервер, на котором запущена версия, отличная от рабочей. Разработчики могут использовать версию Xcode, отличную от той, которая использовалась для развертывания.

**Приложение iOS-фактор разработано для [непрерывного развёртывания](https://avc.com/2011/02/continuous-deployment/) благодаря минимизации различий между разработкой и работой приложения** Рассмотрим три различия, описанных выше:

- Сделать различие во времени небольшим: разработчик может написать код, и он будет развёрнут через несколько часов или даже минут.
- Сделать небольшими различия персонала: разработчик который написал код, активно участвует в его развёртывании и наблюдает за его поведением во время работы приложения.
- Сделать различия инструментов небольшими: держать окружение разработки и работы приложения максимально похожими.. Следуйте принципам фактора [Зависимости](/dependencies) из iOS-factor используйте `.xcode-version` файл, а также описать все другие зависимости явно.

Суммируя вышесказанное в таблицу:

|          | Стандартное iOS приложение | iOS-factor приложение |
|----------|---------------------|----------------|
| Время между развёртываниями | Месяцы  | Дни           |
| Автор кода/тот кто разворачивает | Один человек знает как развернуть проект | Непрерывное развёртывания, в идеале на сервере |
| Окружение разработки/работы приложения  | Различные |  Максимально похожие |
