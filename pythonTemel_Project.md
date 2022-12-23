##### ***1- Bir `listeyi düzleştiren (flatten)` fonksiyon yazın. Elemanları birden çok katmanlı listelerden ( [  [3]  ,  2 ] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:***

>input: &nbsp;&nbsp;&nbsp;[ [ 1, 'a', [ 'cat' ], 2 ], [ [ [ 3 ] ], 'dog' ], 4, 5 ]

>output:&nbsp;&nbsp;[ 1, ' a ', 'cat', 2, 3, 'dog', 4, 5 ]

```python

def flatten(inputList: list) -> None:
    newList=[]
    for _ in inputList:
        if type(_) == list:
            newList.extend(flatten(_))
        else:
            newList.append(_)
    return newList
    
```

##### ***2- Verilen `listenin içindeki elemanları tersine döndüren` bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:***

>input: &nbsp;&nbsp;&nbsp;[ [ 1, 2 ], [ 3, 4 ], [ 5, 6, 7 ] ]

>output: [ [ [ 7, 6, 5], [4, 3], [2, 1]]

```python

def reverseFunc(inputList:list) -> None:
    reversedList=[]

    for sublist in reversed(inputList):
        if type(sublist)==list:
            reversedList.append(sublist[::-1])
        else:
            reversedList.append(sublist)
        

    return reversedList
    
```

