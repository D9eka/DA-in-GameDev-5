# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #5 выполнил(а):
- Барчанинов Иван Николаевич
- РИ-220947

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

## Цель работы
Познакомиться с программными средствами для создания системы машинного обучения и ее интеграции в Unity.

## Задание 1
### Найдите внутри C# скрипта “коэффициент корреляции” и сделать выводы о том, как он влияет на обучение модели.

```cs
float distanceToTarget = Vector3.Distance(this.transform.localPosition, Target.localPosition);

if(distanceToTarget < 1.42f)
{
    SetReward(1.0f);
    EndEpisode();
}
```

Коэффициент корреляции определяет, насколько близко объект должен находиться к цели, чтобы считаться успешным. Его увеличение сделает задачу более легкой, так как агент будет получать награду, находясь от объекта на большем расстоянии.

## Задание 2
### Изменить параметры файла yaml-агента и определить какие параметры и как влияют на обучение модели. Привести описание не менее трех параметров.

- **num_epoch**. Определяет количество эпох обучения. Увеличение параметра улучшает точность обучения, но увеличивает время обучения.
- **batch_size**. Размер пакета определяет, сколько примеров данных используется для обновления модели _за одну итерацию обучения_. Большие размеры обычно ускоряют обучение, но могут потреблять больше памяти. Малые размеры могут оказаться более шумными, но могут помочь модели лучше обобщать.
- **learning_rate**. Скорость обучения определяет, насколько быстро модель _адаптируется к обучающим данным_. Этот параметр контролирует скорость изменения весов модели во время обучения. Если learning rate слишком большой, модель может расходиться. Если слишком мал, то обучение может быть слишком медленным.

## Задание 3
### Приведите примеры, для каких игровых задачи и ситуаций могут использоваться примеры 1 и 2 с ML-Agent’ом. В каких случаях проще использовать ML-агент, а не писать программную реализацию решения?

Пример 1 можно использовать для создания примитивного поведения врага, который ищет игрока и нападает на него. Или для союзника, который следует за игроком.
Пример 2 можно использовать для симуляции поведения NPC в мире. Также этот пример можно использовать для тестирования баланса игры: создать несколько NPC с разными базовыми ресурсами и проверить, кто справится лучше.

Использование ML-агентов оправдано в случаях, когда решение проблемы сложно или неэффективно достижимо с помощью традиционных программных подходов. Например, сложные нелинейные отношения, изменяющаяся среда или автоматизация рутинных задач.

## Выводы

Я познакомился с программными средствами для создания системы машинного обучения и ее интеграции в Unity, посмотрел как работает обучение объектов в Unity, поэскперементировал с параметрами yaml файла, чтобы понять, как они вляют на обучение.

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
