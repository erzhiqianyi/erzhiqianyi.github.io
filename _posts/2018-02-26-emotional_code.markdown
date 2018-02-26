---
layout: post
title: "感情丰富的代码"
date: 2018-02-26 19:43:11 +0800
categories: program
---

```java
public static String doSomeThing(Something someThing){
   String message = "做成功了!";
   if (condition) {
       //do somehing 
       return "没做成功!";
   }
   if(condition1!){
        return "这样不会成功！";
   }
    return message;
}
public static void main(String[] args){
    String message = doSomeThing(new Something());
    if(message == "做成功了!"){
        //do something
    }
}
```

恩，这真的天才的代码!!!!!!!!!!! 代码清晰易懂，简洁明了，情感丰富。我只能膜拜了。

我怎么会知道这么天才的代码呢？我也不知道，上帝说代码要有感情，所以代码就有感情了。
