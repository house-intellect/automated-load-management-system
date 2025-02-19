+++
author = "Менеджер проекта"
title = "Настройка приложения автоматического возврата в коридор допустимой мощности"
date = "2024-12-26"
draft = false
image = "img/blog/news-managed-power-consumption-plot-chart.webp"
description = "Настройка приложения автоматического возврата в коридор допустимой мощности"
tags = [
    "энергосбережение",
    "автоматизация",
    "управление мощностью",
    "промышленная автоматизация",
    "управление энергопотреблением",
]
categories = [
    "технологии",
    "энергосбережения",
]
+++

Управление мощностью осуществляется за счет отключения или включения нагрузок при выходе измеренного значения мощности за пределы допустимого коридора путём считывания данных с цифрового измерительного устройства на вводе и отправки команд телеуправления на управляемые коммутаторы. При значениях мощности ниже нижнего порога гистерезиса коммутаторы нагрузок будут включены, при превышении верхнего порога гистерезиса коммутаторы нагрузок будут отключены согласно созданному в приложении умному сценарию, который при создании принимает на вход следующие параметры: измерительное устройство и вид считываемого измерения, верхний и нижний порог гистерезиса телеметрии, интервал устаревания телеметрии, список задач для выполнения в случае выхода телеметрии из допустимого гистерезисного диапазона.

Повторный выход за пределы гистерезисного диапазона будет последовательно отключать следующие по приоритету коммутаторы после истечения защитных интервалов времени. Перебор приоритетной очереди остановится лишь тогда, когда телеметрия вернется в диапазон.

Начало настройки приложения представляет собой создание периодического опроса измерительного устройства с цифровым интерфейсом связи для получения текущего значения потребляемой мощности и создание задач для выполнения в случае выхода телеметрии из диапазона допустимых значений.

<!--more-->

## Настройка приложения

### Периодический опрос

Первым шагом является настройка периодического опроса измерительного устройства. Это устройство должно иметь цифровой интерфейс связи и предоставлять данные о текущем значении потребляемой мощности.

### Создание сценариев и условий

После настройки опроса необходимо создать сценарии и условия для выполнения сценариев. Эти сценарии сводятся к отправке нескольких последовательных приоритизированных команд на отключение или включение отдельных заранее рассчитанных нагрузок при выходе потребляемой мощности из допустимого диапазона и при ее нормализации с учетом параметров петли гистерезиса.

### Коммутация нагрузок

Будет выделено несколько коммутируемых нагрузок и гистерезисный диапазон значений потребляемой мощности. Приоритеты и интервалы времени между коммутациями, заданные в настройках приложения, будут определять очередность срабатывания коммутаторов нагрузок и характеристики графика коррекции потребляемой мощности.

## Преимущества использования приложения

- **Эффективное управление энергопотреблением**: Автоматический возврат в коридор допустимой мощности позволяет снизить потери энергии и улучшить эффективность работы электрической сети.
- **Гибкость настройки**: Возможность задания приоритетов и интервалов времени между коммутациями позволяет адаптировать работу системы под конкретные условия эксплуатации.
- **Надежность и стабильность**: Использование гистерезисного диапазона значений потребляемой мощности обеспечивает стабильную работу системы и предотвращает частые переключения.

Приложение для автоматического возврата в коридор допустимой мощности является незаменимым инструментом для оптимизации работы электрической сети и повышения ее эффективности.

{{< fullscreen >}}