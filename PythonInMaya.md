---
title: Maya中Python常用函数及参数
date: 2019-05-06 21:28:49
tags: 
	- Maya
	- Python
	- Basic

category: Tech
---

# Maya中Python常用函数及参数


-----
## Pymel.Core 

### pm.select()


{% tabs pm_select %}

<!-- tab <strong>add(add)</strong>  -->
{% label danger@*bool* %}
添加选择
Indicates that the specified items should be added to the active list without removing existing items from the active list.

<!-- endtab -->

<!-- tab <strong>clear(cl)</strong> -->
{% label danger@*bool* %}
取消选择
Clears the active list. This is more efficient than select -d;. Also select -d;
will not remove sets from the active list unless the -neflag is also specified.

<!-- endtab -->



{% endtabs %}



-----

### pm.delete()
**constructionHistory (ch)**    *bool*
>清除历史记录<br>
Remove the construction history on the objects specified or selected.

-----








# Trick

## pm.PopupError()

```python
import pymel.core as pm

try:
    pm.select("RD_01",type = "mesh")
except Exception as e:
    pm.PopupError(str(e))
```
{% note danger %}
报错弹窗
{% endnote %}
