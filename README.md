# FiniteStateAutomaton
#### By Zaostrovskaya Anastasiya


## Дано: 

#### Детерминированный конечный автомат с 0:

#### |Q| = 6 - количество состояний автомата

#### Alf = {0, 1} - алфавит языка, который распознает автомат

## Цель: 
#### Найти конфигурацию автомата, у которого порог синхронизации макисмальный.

Данную задачу решает файл *FSA.py*.
Метод *get_automaton_config* генерирует все возможные конфигурации детерминированного автомата при данных условиях.
Метод *get_conditions_set* генерирует множество состояний, в которое перейдет данное множество по буквам 0 и 1.
Поиск синхронизирующего слова осуществляет метод *bfs* (реализация поиска в ширину - метод обхода графа и поиска пути (слова)).
Представим данную задачу в виде задачи на невзвешенном графе G=(V,E), где V - вершины - всевозможные подмножества множества состояний, Е={(u,v)| u, v ∊ V | есть переход из состояний u в состояния v по букве 1 или 0}.
Поиск заканчивается, когда после прочтения слова остается вершина {0}. 
Конфигурации, у которых порог синхронизации >=10, сохранены в файле *big_words.txt*.

## Запуск: #### py FSA.py
