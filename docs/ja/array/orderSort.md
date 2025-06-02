# orderSort
[[[desc orderSort
  指定された順序 `order` に基づいて、配列 `arr` をソートします。

  `getter` は、配列 `arr` の要素をソートに使用できるキーに変換する関数であり、[getByPath](../object/getByPath) のフィールドパスまたは関数です。

  `getter` が提供されない場合、`orderSort` は配列 `arr` の要素自体をソートのキーとして使用します。

  `order` 配列にない要素は、元の相対的な順序を維持したまま、末尾に配置されます。
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
T:ソートする配列の要素の型
]]]

#### Arguments

[[[params orderSort
arr: ソートする配列
order: 望ましい順序を指定する配列
getter: 配列の要素をソートに使用できるキーに変換します
]]]

#### Returns

[[[returns orderSort

]]]
