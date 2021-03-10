---
title: java8
---

### Stream
1. map

对一个可迭代的对象进行子节点的操作，返回一个新的迭代对象
      
      // 遍历一个list
       List<Integer> numbers=Arrays.asList(3,1,2,4,5,7);
       List<Integer> test2=numbers.stream().map(i->i*i).distinct().collect(Collectors.toList());
     
2. filter

对一个可迭代的对象的子节点
 
       List<String> string= Arrays.asList("abc","","bc","efg","abcd","jkl");
        // filter
       List<String> filter=string.stream().filter(str->!str.isEmpty()).collect(Collectors.toList());

3. forEach

遍历一个可以迭代的集合

    // 遍历一个Map
    
     Map<String,Object> map=new HashMap<String,Object>();
     map.push("a",1);
     map,push("b",3);
     map.forEach((k,v)->System.out.println(kv+));
    // 遍历一个List
    List<String> string= Arrays.asList("abc","","bc","efg","abcd","jkl");
    string.forEach(->System.out::println)

4. parallelStream 并行

5. 统计

 IntSummaryStatistics 类结合Stream
 ```  
    // 该类可以对数字的集合进行平均值，最大值，最小值，合计值
    IntSummaryStatistics statistics=numbers.stream().mapToInt((x)->x).summaryStatistics();
 ```