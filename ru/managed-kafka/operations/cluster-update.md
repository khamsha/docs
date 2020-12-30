# Изменение настроек кластера


После создания кластера {{ KF }} вы можете:
- [Изменить конфигурацию кластера](#update-cluster).
- [Переместить кластер](#move-cluster) из текущего каталога в другой каталог.


{% note warning %}

Если в кластере есть выделенные хосты {{ ZK }}, то вы не сможете изменить их [класс](../concepts/instance-types.md) и настройки. Подробнее см. в разделе [{#T}](../concepts/index.md).

{% endnote %}

## Изменить конфигурацию {#update-cluster}

{% note warning %}

Количество хостов-брокеров {{ KF }} допустимо изменять только в сторону увеличения.

{% endnote %}

{% list tabs %}



- API

  Воспользуйтесь методом API [update](../api-ref/Cluster/update.md) и передайте в запросе:
  - Идентификатор кластера в параметре `clusterId`. Чтобы узнать идентификатор, [получите список кластеров в каталоге](cluster-list.md#list-clusters).
  - Список настроек, которые необходимо изменить, в параметре `updateMask` (одной строкой через запятую). Если не задать этот параметр, метод API сбросит на значения по умолчанию все настройки кластера, которые не были явно указаны в запросе.
  - Новую конфигурацию кластера в параметре `configSpec`.
  

{% endlist %}


## Переместить кластер {#move-cluster}

{% list tabs %}

- API

  Чтобы переместить кластер из текущего каталога в другой, воспользуйтесь методом API [move](../api-ref/Cluster/move.md) и передайте в запросе:
  - Идентификатор кластера в параметре `clusterId`. Чтобы узнать идентификатор, [получите список кластеров в каталоге](cluster-list.md#list-clusters).
  - Идентификатор каталога назначения в параметре `destinationFolderId`.

{% endlist %}
