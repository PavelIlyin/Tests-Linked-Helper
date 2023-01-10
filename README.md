# Tests-Linked-Helper
Задание 1. 
Написать функцию sostavChisla(massivChisel: number[], chislo: number), которая бы находила все возможные комбинации чисел из massivChisel, сумма которых равна chislo. При этом:
-massivChisel содержит, только уникальные положительные числа (> 0)
-в комбинации не должно быть повторений чисел
-все комбинации должны быть уникальными
Задание 2. 
Реализовать асинхронную функцию, которая получает на вход очередь задач Iterable и максимальное кол-во одновременных "потоков" maxThreads и возвращает промис, который будет разрезолвлен, когде все задачи отработают. Функция должна исполнить задачи максимально быстро, стараясь как можно больше задач исполнить параллельно. Но, есть ограничение (в нем заключается основная сложность задачи): в один момент времени Executor не может исполнять несколько разных задач с одним и тем же Task.targetId, но при этом он может исполнять много разных задач с разными Task.targetId параллельно. При взятии задачи из очереди (вызов iterator.next() или итерация через for ... of) она автоматически удаляется из очереди, при этом существующие итераторы не инвалидируются. При этом надо учесть, что очередь может быть пополнена во время исполнения задач, а также, никто не гарантирует, что очередь конечна в принципе. Критерий остановки исполнения функции run(): все полученные из очереди задачи выполнены и в очереди больше нету новых новых задач. Все задачи для одного и того же Task.targetId должны быть исполнены последовательно в том порядке, в котором они находятся в очереди.
