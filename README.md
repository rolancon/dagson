# DAGSON
A JSON seralization format for Direct Acyclic Graphs (DAGs), with optional properties for the DAG, nodes and transisitions.

Version: 0.1

Datetime: 2018-07-29T:57:01Z

##
File extension: `.dag`


![["A", "B"]](imgs/1.png)
["A", "B"]

![["A", "B", "C"]](imgs/2.png)
["A", "B", "C"]

![["A", "B", {{{"name": "graph"}}}]](imgs/3.png)
["A", "B", {{{"name": "graph"}}}]

![test](imgs/4.png)

![test](imgs/5.png)

![test](imgs/6.png)

![test](imgs/7.png)

![test](imgs/8.png)

![test](imgs/9.png)

![test](imgs/10.png)

![test](imgs/11.png)

![test](imgs/12.png)

![test](imgs/13.png)

![test](imgs/14.png)

![test](imgs/15.png)

![test](imgs/16.png)

![test](imgs/17.png)

![test](imgs/18.png)

![test](imgs/19.png)

![test](imgs/20.png)

![test](imgs/21.png)

![test](imgs/22.png)

![test](imgs/23.png)

![test](imgs/24.png)

![test](imgs/25.png)



---

["A", , {"key" "value"}, "B"]

["A", {"key1": "value1", "key2": "value2"}}, "B"]

["A", {"key1": "value1"}, "B", {"key2": "value2"}]

["A", "B", {"key": "value"}]

["A", {"key": "value"}, "B", "C"]

["A", "B", {"key": "value"}, "C"]

["A", "B", "C", {"key": "value"}]

---

[["A", "B"], {"key": "value"}]

["A", "B", "C"], {"key": "value"}]

---

["A", {{"key": "value"}}, "B"]

[["A", "B", "C"], {{"key": "value"}}]

["A", {{"key1": "value1"}}, "B", {{"key2": "value2"}}, "C"]

["A", {"key1": "value1"}, {{"key2": "value2"}}, "B"]

---

[["A", "B"], ["A", "C"]]

[["A", "B", "C"], ["A", "C"]]

[["A", "B"], ["A", "C"], ["A", "D"], ["B", "C"], ["B", "D"], ["C", "D"]]

[["A", "B", "C", "D"], ["A", "C"], ["A", "D"], ["B", "D"]]

---

["A", ["B"], "C"]

["A", ["B", "C"], "C"]

["A", ["B", ["C"], "D"], "C", "D"]

---

[["A", "C"], ["B", "C"]]

---

[["A", ["B", {{"key2": null}}, "C"], "C"], {{"key1": "value1", "key2": "value2"}}]
```
