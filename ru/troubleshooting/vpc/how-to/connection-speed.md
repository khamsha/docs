# Как узнать скорость каналов связи


## Описание проблемы {#issue-description}

Возникла необходимость узнать скорость каналов связи в Yandex Cloud.

## Решение {#case-resolution}

Скорости между различными частями инфраструктуры Yandex Cloud различаются. Итоговая скорость зависит от профиля сетевой нагрузки, мощности конечных точек передачи, качества связывающих каналов, правил обработки трафика на промежуточных узлах.

Скорость между ВМ в одной зоне доступности — в пределах единиц гигабит, между ВМ в разных зонах доступности — сотни мегабит, от ВМ до удалённой точки в глобальной сети — зависит от маршрута. Со своей стороны мы её не ограничиваем, так что она может достигать сотен мегабит.

Тесты можно провести самостоятельно, например, при помощи `iperf`. Мы не приводим конкретных цифр, ведь они сильно зависят от конфигурации ваших ресурсов. Особенно в случае обращения на внешние IP, когда часть трафика идет через маршруты во внешнем интернете, где мы не можем гарантировать какую-либо скорость, поскольку это вне зоны нашей ответственности.