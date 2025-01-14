## Сервис {{ mrd-full-name }} {#managed-redis}

Общие метки для всех метрик сервиса {{ mrd-name }}: 

Метка | Значение
----|----
service | Идентификатор сервиса: `managed-redis`
resource_type | Тип ресурса: `cluster`
resource_id | Идентификатор кластера
host | FQDN хоста
node | Тип хоста: `master`
subcluster_name | Имя подкластера

### Метрики CPU {#managed-redis-cpu-metrics}
Загрузка процессорных ядер.

| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `cpu.fraction`<br/>`DGAUGE`, % | Гарантированная доля vCPU. | 
| `cpu.guarantee`<br/>`DGAUGE`, штуки | Гарантированное число ядер. | 
| `cpu.guest`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `guest`. | 
| `cpu.guest_nice`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `guest_nice`. | 
| `cpu.limit`<br/>`DGAUGE`, штуки | Предельное число используемых ядер. | 
| `cpu.idle`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `idle`. | 
| `cpu.iowait`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `iowait`. | 
| `cpu.irq`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `irq`. | 
| `cpu.nice`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `nice`. | 
| `cpu.softirq`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `softirq`. | 
| `cpu.steal`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `steal`. | 
| `cpu.system`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `system`. | 
| `cpu.user`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `user`. | 
| `cpu_utilization_by_db_15`<br/>`DGAUGE`, % | Средняя утилизация процессорных ядер ВМ (vCPU) базой данных в процентах за 15 секунд. Принимает значения от 0% до [уровня производительности vCPU](../../../compute/concepts/performance-levels.md). | 
| `cpu_utilization_by_db_15_limit`<br/>`DGAUGE`, % | Предельная утилизация процессорных ядер ВМ (vCPU) базой данных в процентах за 15 секунд. | 
| `cpu_utilization_by_db_60`<br/>`DGAUGE`, % | Средняя утилизация процессорных ядер ВМ (vCPU) базой данных в процентах за 60 секунд. | 
| `cpu_utilization_by_db_60_limit`<br/>`DGAUGE`, % | Предельная утилизация процессорных ядер ВМ (vCPU) базой данных в процентах за 60 секунд. |
| `load.avg_15min`<br/>`DGAUGE`, % | Средняя нагрузка за 15 минут. | 
| `load.avg_1min`<br/>`DGAUGE`, % | Средняя нагрузка за 1 минуту. | 
| `load.avg_5min`<br/>`DGAUGE`, % | Средняя нагрузка за 5 минут. |

### Метрики дисковых операций {#managed-redis-diskio-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `io.disk*.iops_in_progress`<br/>`DGAUGE`, штуки | Количество незавершенных дисковых операций. | 
| `io.disk*.merged_reads`<br/>`DGAUGE`, штуки | Количество слитых операций чтения с конкретного диска. | 
| `io.disk*.merged_writes`<br/>`DGAUGE`, штуки | Количество слитых операций записи на конкретный диск. | 
| `io.disk*.read_bytes`<br/>`DGAUGE`, байт/с | Скорость чтения с конкретного диска. | 
| `io.disk*.read_count`<br/>`DGAUGE`, операций/с | Количество операций чтения с конкретного диска в секунду. | 
| `io.disk*.read_time`<br/>`DGAUGE`, миллисекунды | Среднее время чтения с конкретного диска. | 
| `io.disk*.utilization`<br/>`DGAUGE`, % | Утилизация конкретного диска. | 
| `io.disk*.weighted_io_time`<br/>`DGAUGE`, миллисекунды | Длительность ожидания операций ввода/вывода на конкретном диске. | 
| `io.disk*.write_time`<br/>`DGAUGE`, миллисекунды | Среднее время записи на конкретный диск. | 
| `io.disk*.write_bytes`<br/>`DGAUGE`, байт/с | Скорость записи на конкретный диск. | 
| `io.disk*.write_count`<br/>`DGAUGE`, операций/с | Количество операций записи на конкретный диск в секунду. | 

### Метрики RAM {#managed-redis-ram-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `mem.active_bytes`<br/>`DGAUGE`, байты | Объем оперативной памяти, которая используется наиболее часто и освобождается только в крайнем случае. | 
| `mem.available_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `available`. | 
| `mem.available_percent_bytes`<br/>`DGAUGE`, % | Доля использования оперативной памяти, тип потребления `available`. | 
| `mem.buffers_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `buffers`. | 
| `mem.cached_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `cached`. | 
| `mem.commit_limit_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `commit_limit`. | 
| `mem.committed_as_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `committed_as`. | 
| `mem.dirty_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `dirty`. | 
| `mem.free_bytes`<br/>`DGAUGE`, байты | Объем свободной оперативной памяти, доступной для использования, без учета `mem.buffers_bytes` и `mem.cached_bytes`. |
| `mem.high_free_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `high_free`. | 
| `mem.high_total_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `high_total`. | 
| `mem.huge_page_size_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `huge_page_size`. | 
| `mem.huge_pages_free_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `huge_pages_free`. | 
| `mem.huge_pages_total_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `huge_pages_total`. | 
| `mem.inactive_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `inactive`. | 
| `mem.low_free_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `low_free`. | 
| `mem.low_total_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `low_total`. | 
| `mem.mapped_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `mapped`. | 
| `mem.page_tables_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `page_tables`. | 
| `mem.shared_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `shared`. | 
| `mem.slab_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `slab`. | 
| `mem.sreclaimable_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `sreclaimable`. | 
| `mem.sunreclaim_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `sunreclaim`. | 
| `mem.swap_cached_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `swap_cached`. | 
| `mem.swap_free_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `swap_free`. | 
| `mem.swap_total_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `swap_total`. | 
| `mem.total_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `total`. | 
| `mem.used_bytes`<br/>`DGAUGE`, байты | Объем оперативной памяти, которую в данный момент используют запущенные процессы. | 
| `mem.used_percent_bytes`<br/>`DGAUGE`, % | Процент использованной оперативной памяти. | 
| `mem.vmalloc_chunk_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `vmalloc_chunk`. | 
| `mem.vmalloc_total_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `vmalloc_total`. | 
| `mem.vmalloc_used_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `vmalloc_used`. | 
| `mem.write_back_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `write_back`. | 
| `mem.write_back_tmp_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `write_back_tmp`. |

### Метрики сети {#managed-redis-net-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `net.bytes_recv`<br/>`DGAUGE`, байт/с | Скорость получения данных по сети. | 
| `net.bytes_sent`<br/>`DGAUGE`, байт/с | Скорость отправки данных по сети. | 
| `net.drop_in`<br/>`DGAUGE`, штуки | Количество пакетов, отброшенных при получении. | 
| `net.drop_out`<br/>`DGAUGE`, штуки | Количество пакетов, отброшенных при отправке. | 
| `net.err_in`<br/>`DGAUGE`, штуки | Количество ошибок при получении. | 
| `net.err_out`<br/>`DGAUGE`, штуки | Количество ошибок при отправке. | 
| `net.packets_recv`<br/>`DGAUGE`, пакетов/с | Интенсивность получения данных по сети. | 
| `net.packets_sent`<br/>`DGAUGE`, пакетов/с | Интенсивность отправки данных по сети. |

### Метрики сервиса {#managed-redis-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `active`<br/>`DGAUGE`, штуки | Количество активных кластеров. |
| `available`<br/>`DGAUGE`, штуки | Количество доступных кластеров. |
| `available_percent`<br/>`DGAUGE`, % | Доля доступных кластеров. |
| `buffered`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `buffered`. |
| `bytes_recv`<br/>`DGAUGE`, байты | Размер полученных данных. |
| `bytes_sent`<br/>`DGAUGE`, байты | Размер отправленных данных. |
| `cached`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `cached`. |
| `commit_limit`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `commit_limit`. |
| `committed_as`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `committed_as`. |
| `dirty`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `dirty`. | 
| `drop_in`<br/>`DGAUGE`, штуки | Количество пакетов, отброшенных при получении. | 
| `drop_out`<br/>`DGAUGE`, штуки | Количество пакетов, отброшенных при отправке. | 
| `err_in`<br/>`DGAUGE`, штуки | Количество ошибок при получении. | 
| `err_out`<br/>`DGAUGE`, штуки | Количество ошибок при отправке. | 
| `free`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `free`. | 
| `high_free`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `high_free`. | 
| `high_total`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `high_total`. | 
| `huge_page_size`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `huge_page_size`. | 
| `huge_pages_free`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `huge_pages_free`. | 
| `huge_pages_total`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `huge_pages_total`. | 
| `icmp_inaddrmasks`<br/>`DGAUGE`, штуки | Количество полученных сообщений с запросом маски ICMP-адреса. | 
| `icmp_incsumerrors`<br/>`DGAUGE`, штуки | Общее количество IP-пакетов с ошибками контрольной суммы. | 
| `icmp_indestunreachs`<br/>`DGAUGE`, штуки | Количество полученных сообщений о недоступности назначения ICMP. | 
| `icmp_inechos`<br/>`DGAUGE`, штуки | Количество полученных ICMP-сообщений Echo (запросов). | 
| `icmp_inparmprobs`<br/>`DGAUGE`, штуки | Количество полученных сообщений о неполадках с параметрами ICMP. | 
| `icmp_inredirects`<br/>`DGAUGE`, штуки | Количество полученных сообщений о перенаправлении ICMP. | 
| `icmp_insrcquenchs`<br/>`DGAUGE`, штуки | Количество полученных ICMP-сообщений Source Quench. | 
| `icmp_intimeexcds`<br/>`DGAUGE`, штуки | Количество полученных сообщений с превышением времени ICMP превысило количество полученных сообщений. | 
| `icmp_intimestampreps`<br/>`DGAUGE`, штуки | Количество полученных ответных сообщений с меткой времени ICMP. | 
| `icmp_outaddrmaskreps`<br/>`DGAUGE`, штуки | Количество отправленных ответных сообщений по маске ICMP-адреса. | 
| `icmp_outaddrmasks`<br/>`DGAUGE`, штуки | Количество отправленных сообщений с запросом маски ICMP-адреса. | 
| `icmp_outdestunreachs`<br/>`DGAUGE`, штуки | Количество отправленных сообщений о недоступности назначения ICMP. | 
| `icmp_outechoreps`<br/>`DGAUGE`, штуки | Количество отправленных ICMP-сообщений Echo Reply. | 
| `icmp_outechos`<br/>`DGAUGE`, штуки | Количество отправленных ICMP-сообщений Echo (запросов). | 
| `icmp_outerrors`<br/>`DGAUGE`, штуки | Количество ICMP-сообщений, которые этот объект не отправил из-за проблем, обнаруженных в ICMP, таких как нехватка буферов. | 
| `icmp_outparmprobs`<br/>`DGAUGE`, штуки | Количество отправленных сообщений о проблемах с параметрами ICMP. | 
| `icmp_outtimeexcds`<br/>`DGAUGE`, штуки | Количество отправленных сообщений с превышением времени ICMP превысило количество отправленных сообщений. | 
| `icmp_outtimestampreps`<br/>`DGAUGE`, штуки | Количество отправленных ответных сообщений с меткой времени ICMP. | 
| `inactive`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `inactive`. | 
| `iops_in_progress`<br/>`DGAUGE`, штуки | Количество незавершенных дисковых операций. | 
| `ip_defaultttl`<br/>`DGAUGE`, строка | Значение по умолчанию, вставляемое в поле Time-To-Live заголовка IP-пакетов, созданных в этом объекте, когда значение TTL не предоставляется протоколом транспортного уровня. | 
| `ip_forwdatagrams`<br/>`DGAUGE`, штуки | Количество входящих пакетов, для которых этот объект не был их конечным IP-адресатом, в результате чего была предпринята попытка найти маршрут для пересылки их в этот конечный пункт назначения. В объектах, которые не действуют как IP-маршрутизаторы, этот счетчик будет включать только те пакеты, которые были перенаправлены источником через этот объект, и обработка параметра исходного маршрута прошла успешно. | 
| `ip_fragcreates`<br/>`DGAUGE`, штуки | Количество фрагментов IP-пакетов, которые были сгенерированы в результате фрагментации в этом объекте. | 
| `ip_fragfails`<br/>`DGAUGE`, штуки | Количество IP-пакетов, которые были отброшены, поскольку они должны были быть фрагментированы в этом объекте, но не могли быть фрагментированы, например, потому что был установлен флаг, запрещающий фрагментацию. | 
| `ip_inaddrerrors`<br/>`DGAUGE`, штуки | Количество входящих пакетов, отброшенных из-за того, что IP-адрес в поле назначения их IP-заголовка не был допустимым адресом для получения в этом объекте. Это количество включает недопустимые адреса (например, `0.0.0.0`) и адреса неподдерживаемых классов (например, класс E). Для объектов, которые не являются IP-маршрутизаторами и, следовательно, не пересылают пакеты, этот счетчик включает пакеты, отброшенные из-за того, что адрес назначения не был локальным адресом. | 
| `ip_indiscards`<br/>`DGAUGE`, штуки | Количество входящих IP-пакетов, для которых не возникло проблем, препятствующих их дальнейшей обработке, но которые были отброшены (например, из-за нехватки места в буфере). Этот счетчик не включает в себя пакеты, отброшенные в ожидании повторной сборки. | 
| `ip_inreceives`<br/>`DGAUGE`, штуки | Общее количество входящих пакетов, полученных от интерфейсов, включая полученные по ошибке. | 
| `ip_outdiscards`<br/>`DGAUGE`, штуки | Количество выходящих IP-пакетов, для которых не возникло проблем, препятствующих их передаче по назначению, но которые были отброшены (например, из-за нехватки места в буфере). Обратите внимание, что этот счетчик включал бы пакеты, подсчитанные в `ip_forwdatagrams`, если бы такие пакеты удовлетворяли этому (дискреционному) критерию отбрасывания. | 
| `ip_outnoroutes`<br/>`DGAUGE`, штуки | Количество отброшенных IP-пакетов, для которых не удалось найти маршрут для их передачи по назначению. Этот счетчик включает все пакеты, подсчитанные в `ip_forwdatagrams`, которые соответствуют критерию «без маршрута». Сюда входят любые пакеты, которые хост не может перенаправить, поскольку все его маршрутизаторы по умолчанию не работают. | 
| `ip_outrequests`<br/>`DGAUGE`, штуки | Общее количество IP-пакетов, которые локальные пользовательские протоколы IP (включая ICMP) передали IP в запросах на передачу. Этот счетчик не включает в себя пакеты, подсчитанные в `ip_forwdatagrams`. | 
| `ip_reasmfails`<br/>`DGAUGE`, штуки | Количество сбоев, обнаруженных алгоритмом повторной сборки IP (по любой причине: тайм-аут, ошибки и т.д.). Это не обязательно количество отброшенных IP-фрагментов, поскольку некоторые алгоритмы (в частности, алгоритм в RFC 815) могут потерять отслеживание количества фрагментов, объединяя их по мере их получения. | 
| `ip_reasmoks`<br/>`DGAUGE`, штуки | Количество IP-пакетов, успешно собранных повторно. | 
| `ip_reasmreqds`<br/>`DGAUGE`, штуки | Количество полученных IP-фрагментов, которые необходимо было повторно собрать в этом объекте. | 
| `ip_reasmtimeout`<br/>`DGAUGE`, секунды | Максимальное количество секунд, в течение которых удерживаются полученные фрагменты, пока они ожидают повторной сборки в этом объекте. | 
| `low_free`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `low_free`. | 
| `low_total`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `low_total`. | 
| `mapped`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `mapped`. | 
| `merged_reads`<br/>`DGAUGE`, штуки | Количество слитых операций чтения с дисков. | 
| `merged_writes`<br/>`DGAUGE`, штуки | Количество слитых операций записи на диски. | 
| `n_cpus`<br/>`DGAUGE`, штуки | Предельное число используемых ядер. | 
| `n_users`<br/>`DGAUGE`, штуки | Предельное число пользователей. | 
| `packets_recv`<br/>`DGAUGE`, пакетов/с | Интенсивность получения данных по сети. | 
| `packets_sent`<br/>`DGAUGE`, пакетов/с | Интенсивность отправки данных по сети. | 
| `page_tables`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `page_tables`. | 
| `read_bytes`<br/>`DGAUGE`, байт/с | Скорость чтения с конкретного диска. | 
| `read_count`<br/>`DGAUGE`, операций/с | Количество операций чтения с конкретного диска в секунду. | 
| `read_time`<br/>`DGAUGE`, миллисекунды | Среднее время чтения с дисков. | 
| `shared`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `shared`. | 
| `slab`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `slab`. | 
| `sreclaimable`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `sreclaimable`. | 
| `sunreclaim`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `sunreclaim`. | 
| `swap_cached`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `swap_cached`. | 
| `swap_free`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `swap_free`. | 
| `swap_total`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `swap_total`. | 
| `tcp_activeopens`<br/>`DGAUGE`, штуки | Количество раз, когда TCP-соединения совершали прямой переход из состояния `CLOSED` в состояние `SYN-SENT`. | 
| `tcp_attemptfails`<br/>`DGAUGE`, штуки | Количество раз, когда TCP-соединения совершали прямой переход в состояние `CLOSED` либо из состояния `SYN-SENT`, либо из состояния `SYN-RCVD`, плюс количество раз, когда TCP-соединения совершали прямой переход. | 
| `tcp_currestab`<br/>`DGAUGE`, штуки | Текущее количество TCP-соединений для состояния `ESTABLISHED` или `CLOSE WAIT`. | 
| `tcp_estabresets`<br/>`DGAUGE`, штуки | Количество раз, когда TCP-соединения совершали прямой переход в состояние `CLOSED` либо из состояния `ESTABLISHED`, либо из состояния `CLOSE-WAIT`. | 
| `tcp_incsumerrors`<br/>`DGAUGE`, штуки | Увеличивается, когда полученный TCP-пакет имеет неправильную контрольную сумму. | 
| `tcp_insegs`<br/>`DGAUGE`, штуки | Общее количество полученных сегментов, включая те, которые были получены по ошибке. | 
| `tcp_passiveopens`<br/>`DGAUGE`, штуки | Количество раз, когда TCP-соединения осуществляли прямой переход в состояние `SYN-RCVD` из состояния `LISTEN`. | 
| `tcp_retranssegs`<br/>`DGAUGE`, штуки | Общее количество повторно переданных сегментов, то есть количество переданных TCP-сегментов, содержащих один или несколько ранее переданных октетов. | 
| `tcp_rtomax`<br/>`DGAUGE`, штуки | Максимальное значение, разрешенное реализацией TCP для времени ожидания повторной передачи, измеряемое в миллисекундах. | 
| `tcp_rtomin`<br/>`DGAUGE`, штуки | Минимальное значение, разрешенное реализацией TCP для времени ожидания повторной передачи, измеряемое в миллисекундах. | 
| `total`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `total`. | 
| `udp_ignoredmulti`<br/>`DGAUGE`, штуки | Для многоадресной рассылки UDP. | 
| `udp_incsumerrors`<br/>`DGAUGE`, штуки | Увеличивается, когда полученный UDP-пакет содержит недопустимую контрольную сумму кода ядра. | 
| `udp_noports`<br/>`DGAUGE`, штуки | Общее количество полученных UDP-пакетов, для которых на порту назначения не было приложения. | 
| `udp_outdatagrams`<br/>`DGAUGE`, штуки | Общее количество UDP-пакетов, отправленных от этого объекта. | 
| `udplite_incsumerrors`<br/>`DGAUGE`, штуки | Увеличивается, когда полученный пакет UDP Lite содержит недопустимую контрольную сумму кода ядра. | 
| `udplite_noports`<br/>`DGAUGE`, штуки | Общее количество принятых пакетов UDP Lite, для которых на порте назначения не было слушателя. Перебои в значении этого счетчика могут возникать при повторной инициализации системы управления и в другое время, на что указывает значение `udplite_statsdiscontinuitytime`. | 
| `udplite_rcvbuferrors`<br/>`DGAUGE`, штуки | Увеличивается, когда память не может быть выделена для обработки входящего пакета UDP Lite. | 
| `udplite_sndbuferrors`<br/>`DGAUGE`, штуки | Увеличивается, когда память не может быть выделена для отправки пакета UDP Lite. | 
| `uptime`<br/>`DGAUGE`, % | Коэффициент отказоустойчивости. | 
| `usage_guest`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `guest`. | 
| `usage_guest_nice`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `guest_nice`. | 
| `usage_idle`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `idle`. | 
| `usage_iowait`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `iowait`. | 
| `usage_irq`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `irq`. | 
| `usage_nice`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `nice`. | 
| `usage_softirq`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `softirq`. | 
| `usage_steal`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `steal`. | 
| `usage_system`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `system`. | 
| `usage_user`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `user`. | 
| `used`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `used`. | 
| `used_percent`<br/>`DGAUGE`, % | Доля использования оперативной памяти, тип потребления `used`. | 
| `utilization`<br/>`DGAUGE`, % | Средняя утилизация процессорных ядер ВМ (vCPU) базой данных. | 
| `vmalloc_chunk`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `vmalloc_chunk`. | 
| `vmalloc_total`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `vmalloc_total`. | 
| `vmalloc_used`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `vmalloc_used`. | 
| `weighted_io_time`<br/>`DGAUGE`, миллисекунды | Длительность ожидания операций ввода/вывода. | 
| `write_back`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `write_back`. | 
| `write_back_tmp`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `write_back_tmp`. |
| `write_bytes`<br/>`DGAUGE`, байт/с | Скорость записи на диски. | 
| `write_count`<br/>`DGAUGE`, операций/с | Количество операций записи в секунду. | 
| `write_time`<br/>`DGAUGE`, миллисекунды | Среднее время записи на диски. | 

Подробнее о сервисе в документации [{{ mrd-name }}](../../../managed-redis/).
