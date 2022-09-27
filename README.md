# Merge Sort Projesi

Merhaba, [Patika](https://www.patika.dev)'nın [Veri Yapıları Ve Algoritmalar](https://app.patika.dev/courses/veri-yapilari-ve-algoritmalar) eğitimi kapsamındaki 2. Projesini tamamladım.

## [16,21,11,8,12,22] -> Merge Sort

**1. Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.**

***Cevap***

İlk olarak dizide tek eleman kalana kadar ikiye bölme işlemi yapılır.

|    |    |    |    |    |    |   |    |    |    |    |    |
| -- | -- | -- | -- | -- | -- | - | -- | -- | -- | -- | -- |
|    |    |    | 16 | 21 | 11 | 8 | 12 | 22 |    |    |    |
|    |    | 16 | 21 | 11 |    |   | 8  | 12 | 22 |    |    |
|    | 16 | 21 |    | 11 |    |   | 8  |    | 12 | 22 |    |
| 16 |    | 21 |    | 11 |    |   | 8  |    | 12 |    | 22 |

Daha sonra tek başına duran elemanlar sıralı olacak şekilde adım adım birleştirilir.

|    |    |    |    |    |    |    |    |    |    |    |    |
| -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| 16 |    | 21 |    | 11 |    |    | 8  |    | 12 |    | 22 |
|    | 16 | 21 |    | 11 |    |    | 8  |    | 12 | 22 |    |
|    |    | 11 | 16 | 21 |    |    | 8  | 12 | 22 |    |    |
|    |    |    | 8  | 11 | 12 | 16 | 21 | 22 |    |    |    |

---

**2. Big-O gösterimini yazınız.**

***Cevap***

Dizimizin eleman sayısını n olarak düşünürsek her bir adımda o anki adımda bulunan eleman sayısının bir eksiği kadar karşılaştırma işlemi yapıyoruz. Bunu Big O notasyonunda O(n) olarak ele alabiliriz. Aynı zamanda dizimizi her seferinde iki parçaya bölüyoruz. Bu durumun da Big O notasyonunu O(logn) olarak ele alabiliriz. Sonuç olarak bu iki notasyonu birleştirince de O(nlogn) sonucuna varıyoruz.
