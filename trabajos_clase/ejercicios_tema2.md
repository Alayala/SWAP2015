#### Ejercicio T2.1: Calcular la disponibilidad del sistema descrito en edgeblog.net si tenemos dos réplicas de cada elemento salvo para el centro de datos (en total 3 elementos en cada subsistema).

* Tabla con componentes replicados una vez

| Componente | Disponibilidad |
| :--------- | :-------------:|
|	Web        | 97.75%         |
| Application| 99%            |
| Database   | 99.9999%       |
| DNS        | 99.96%         |
| Firewall   | 97.75%         |
| Switch     | 99.99%         |
| Data Center| 99.99%         |
| ISP        | 99.75%         |

- Realizamos los cálculos necesarios para realizar la segunda réplica:

| Componente | Cálculo                         |Disponibilidad |
| :--------- | :------------------------------ |:-------------:|
|	Web        | 0.9775 + (1 - 0.9775) * 0.85    | 99.6625%      |
| Application| 0.99 + (1 - 0.99) * 0.9         | 99.9%         |
| Database   | 0.999999 + (1 - 0.999999) * 0999| 99.999999999% |
| DNS        | 0.9996 + (1 - 0.9996) * 0.98    | 99.9992%      |
| Firewall   | 0.9775 + (1 - 0.9775) * 0.85    | 99.6625%      |
| Switch     | 0.9999 + (1 - 0.9999) * 0.99    | 99.9999%      |
| ISP        | 0.9975 + (1 - 0.9975) * 0.95    | 99.9875%      |

- Calculamos la disponibilidad del sistema:

99.6625% * 99.9% * 99.999999999% * 99.9992% * 99.6625% * 99.9999% * 99.9875% = 99.2135%

La disponibilidad global del sistema, replicando dos veces la mayoría de los componentes es de un: 99.2135%.
