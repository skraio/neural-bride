# Лабораторная 2 по курсу "Технологии искусственного интеллекта"

### Описание:
1. Невеста ищет себе жениха (существует единственное вакантное место).
2. Число претендентов - N.
3. Невеста общается с претендентами в случайном порядке, с каждым не более одного раза.
4. О каждом претенденте известно, лучше он или хуже любого из предыдущих.
5. Пообщавшись с претендентом, невеста сравнивает его с предыдущими и либо отказывает, либо
   принимает его предложение. Если предложение принято, они женятся и процесс останавливается. Если
   невеста отказывает жениху, то вернуться к нему позже она не сможет.
6. Невеста выигрывает, если она выберет самого лучшего претендента. Выбор даже второго по порядку
   сравнения - проигрыш.

### Задача:
1. Разработать и обучить нейронную сеть, которая возьмет на себя роль невесты и будет решать принять
   предложение или отказать очередному жениху.
2. Сравнить результат принятия решения обученной нейронной сети и оптимальным математическим
   алгоритмом.

## Реализация:

Реализация предоставлена в ноутбуке [rl_ppo.ipynb](rl_ppo.ipynb).

В процессе реализации для выбора подходящего алгоритма обучения с подкреплением изначально был
использован алгоритм DQN. Однако результаты обучения оказались недостаточно точными для решения
задачи. Для улучшения качества работы модели было решено заменить DQN на PPO - более продвинутый
алгоритм, который лучше показал себя в данной задаче и обеспечил более стабильные успешности.

## Результаты

Результаты предоставлены в ноутбуке [rl_ppo.ipynb](rl_ppo.ipynb).

Обучение модели показало улучшение успешности в процессе тренировок, достигнув значений, близких к
теоретическому оптимуму в 0.37.

При обучении, успехи модели на ранних этапах постепенно увеличивались: к 50 000 шагу успешность
модели составила 0.37, и дальнейшие тренировки показали стабильные, но колеблющиеся результаты. На
финальном этапе обучения успешность модели оставалась в диапазоне от 0.35 до 0.45.

Эпизоды показали аналогичные данные: на промежутке с 300 по 500 эпизоды успешность стабилизировалась
на уровне 0.36, что примерно соответствует оптимальной успешности выбора лучшего претендента.

Итоговая успешность RL-модели составила 0.357, что практически совпадает с теоретическим оптимумом,
подтверждая эффективность выбранного подхода, хотя стабильность модели могла бы быть выше.

## Выполнил
- Каримов Аскар, гр. М8О-208М-23
