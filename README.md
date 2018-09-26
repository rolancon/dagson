# DAGSON
A JSON seralization format for Direct Acyclic Graphs (DAGs), with optional properties for the DAG, nodes and transitions.

Version: 0.1

Datetime: 2018-07-29T:57:01Z

File extension: `.dag`

## Simple nodes

![["A", "B"]](imgs/1.png)
["A", "B"]

![["A", "B", "C"]](imgs/2.png)
["A", "B", "C"]

![["A", "B", {{{"name": "graph"}}}]](imgs/3.png)
["A", "B", {{{"name": "graph"}}}]

## Nodes with properties

![["A", {"key" "value"}, "B"]](imgs/4.png)
["A", {"key" "value"}, "B"]

![["A", {"key1": "value1", "key2": "value2"}}, "B"]](imgs/5.png)
["A", {"key1": "value1", "key2": "value2"}}, "B"]

![["A", {"key1": "value1"}, "B", {"key2": "value2"}]](imgs/6.png)
["A", {"key1": "value1"}, "B", {"key2": "value2"}]

![["A", "B", {"key": "value"}]](imgs/7.png)
["A", "B", {"key": "value"}]

![["A", {"key": "value"}, "B", "C"]](imgs/8.png)
["A", {"key": "value"}, "B", "C"]

![["A", "B", {"key": "value"}, "C"]](imgs/9.png)
["A", "B", {"key": "value"}, "C"]

![["A", "B", "C", {"key": "value"}]](imgs/10.png)
["A", "B", "C", {"key": "value"}]

## Nodes with same properties

![[["A", "B"], {"key": "value"}]](imgs/11.png)
[["A", "B"], {"key": "value"}]

![[["A", "B", "C"], {"key": "value"}]](imgs/12.png)
[["A", "B", "C"], {"key": "value"}]

## Transitions with properties

![["A", {{"key": "value"}}, "B"]](imgs/13.png)
["A", {{"key": "value"}}, "B"]

![[["A", "B", "C"], {{"key": "value"}}]](imgs/14.png)
[["A", "B", "C"], {{"key": "value"}}]

![["A", {{"key1": "value1"}}, "B", {{"key2": "value2"}}, "C"]](imgs/15.png)
["A", {{"key1": "value1"}}, "B", {{"key2": "value2"}}, "C"]

![["A", {"key1": "value1"}, {{"key2": "value2"}}, "B"]](imgs/16.png)
["A", {"key1": "value1"}, {{"key2": "value2"}}, "B"]

## Grouped nodes

![[["A", "B"], ["A", "C"]]](imgs/17.png)
[["A", "B"], ["A", "C"]]

![[["A", "B", "C"], ["A", "C"]]](imgs/18.png)
[["A", "B", "C"], ["A", "C"]]

![[["A", "B"], ["A", "C"], ["A", "D"], ["B", "C"], ["B", "D"], ["C", "D"]]](imgs/19.png)
[["A", "B"], ["A", "C"], ["A", "D"], ["B", "C"], ["B", "D"], ["C", "D"]]

![[["A", "B", "C", "D"], ["A", "C"], ["A", "D"], ["B", "D"]]](imgs/20.png)
[["A", "B", "C", "D"], ["A", "C"], ["A", "D"], ["B", "D"]]

## Nested nodes

![["A", ["B"], "C"]](imgs/21.png)
["A", ["B"], "C"]

![["A", ["B", "C"], "C"]](imgs/22.png)
["A", ["B", "C"], "C"]

![["A", ["B", ["C"], "D"], "C", "D"]](imgs/23.png)
["A", ["B", ["C"], "D"], "C", "D"]

## Graph with two start nodes

![[["A", "C"], ["B", "C"]]](imgs/24.png)
[["A", "C"], ["B", "C"]]

## Transition with overriden common property

![[["A", ["B", {{"key2": null}}, "C"], "C"], {{"key1": "value1", "key2": "value2"}}]](imgs/25.png)
[["A", ["B", {{"key2": null}}, "C"], "C"], {{"key1": "value1", "key2": "value2"}}]
