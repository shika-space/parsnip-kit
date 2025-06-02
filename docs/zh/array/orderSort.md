# orderSort
[[[desc orderSort
  根据指定的顺序 `order` 对数组 `arr` 进行排序。

  `getter` 是一个将数组 `arr` 的元素转换为可用于排序的 key 的函数，它可以是 [getByPath](../object/getByPath) 的字段路径或一个函数。如果未提供 `getter`，`orderSort` 将使用数组 `arr` 的元素本身作为排序的 key。

  不在 `order` 数组中的元素将保持它们原来的顺序排在末尾。
]]]
[[[version orderSort
  
]]]

### Usage

```ts
import { orderSort } from 'parsnip-kit'

const arr = [{ id: 0 }, { id: 2 }, { id: 1 }, { id: 3 }, { id: 4 }]
const order = [1, 3, 2]
const getter = (item: { id: number }) => item.id

const sortedArr = orderSort(arr, order, getter)
// [{ id: 1 }, { id: 3 }, { id: 2 }, { id: 0 }, { id: 4 }]
```


### API

#### Type Parameter

[[[template orderSort
T:要排序的数组元素类型
]]]

#### Arguments

[[[params orderSort
arr: 要排序的数组
order: 指定期望顺序的数组
getter: 将数组的元素转换为可用于排序的 key
]]]

#### Returns

[[[returns orderSort

]]]
