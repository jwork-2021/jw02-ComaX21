### example类图
![](http://www.plantuml.com/plantuml/png/ZL9BJW914DtFANe98NC1um99HZGnOFYWYN7HG8aJcvv9Vw9eN1bTUWJNheokFOyXtiA2giR6Jy9iwbLDVTwhhhfrqZW_LKcIQmVcJ8v0T0k3y2OH-DLK8SULAc6BFmAUW3jKKgDxcoGZ9QqL3JySAeYhKsnwSYeaELrdSZqH9PPjs9lgxAKiQGxr5jjfkZPCR7syFCqVNvDOnK6k9MQm38ij2vkxlD3nbD-XWLGUQ1feFnNDmfinDMctCh44lQCsWxrEnh7TTh_3A1zmhBj_p20RP2s2QKh6i3jXErpxNJDIN_p1AlXBLerPXxCsLxZOvS-OA-XbI3NlRR5a4XzjbzuvrFCRXm95bdGW6ux75u8XuAhG1C-ZP6W5yIbzV0dVB7UCaRD_IHFZq1P9Fzn_tZtFtzx3y2R0zUemoH7k70XHbC_9abbHw8MiIbMibasvWGwAXtx9NbfAOo4-ORY2aNUyYpheiP-gBm00)

### example时序图
![](http://www.plantuml.com/plantuml/png/L8vB2W9134JtEKLTG6-WkFCSpL23WJPfqfaPyVJ-6zmz7Y-aJZrBv7Aj46bFqabRiKHLevGfFP0Ndiaxuo_e7id0jt7Z3tDpZClWyBClCLZNuRlU1dAbGKHUtx4xVbQO9r4vvrllctTDTUiumBZXKIVPh4GCGr5udwVe8_W_C2iVmRsuqwq-W-WujMGK1_of2X9mj5ZKHHVMrEBBvDwqR-4bkKID3dJJVlUSddEJ3NxV76m9k2twgpj8Bqtz3EaDD7fWwYVJJcpx8dPsjnFd9SJUj_qmiMKEezaQJr7y62qpSdLYkCZGrOlOAZDNDs9BpAX-Z5OOkNN4S85Xs54udc62MKRrpSV4V2hSVpNwtZQvJT_e4NnUVmHuCWLz2ddnQvfdlC19QTepqdHdPPSzG75Whmz9todPAqqktWAEfbYfuFl_dmCE4V3Y7QlpkIbu2Pn17jlHuqyToZ7AcM_VZoK52o5fZBuBiKuNm5_qBm00)

### example理解（个人观点）
#### 优点：
1. 类分离的好，对于葫芦娃的信息，只有老爷爷知道，而排序器只知道一串数字，没有访问葫芦娃类。
2. 类抽象的好，首先有了接口类Linable和Sorter，抽象出了可排队元素和排序器的共同功能，<br>然后在具体的类Gourd和BubbleSorter中实现了接口。
#### 缺点：
1. Position类没有必要定义成Line的内部类
2. 相比于将七个葫芦娃定义为枚举类型，我更倾向于定义为一个类。<br>例如现在我想要把每个葫芦娃的能力也定义出来，<br>这个时候如果定义为类可以通过定义子类进行继承来实现。
3. 没有看出在Geezer类中定义theGeezer的作用