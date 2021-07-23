# let const var 区别


变量提升的区别，变量提升是指存储在内存当中，不是立即使用的变量，可以先使用后声明，只有var会变量提升，let const不会。

    var a
    console.log(a)  // undefined
    a = 1
    console.log(a)  // 1
    
在代码块中声明val等于在外部声明，let在内部声明外部无法访问

    if(true){
      var a = 1
      let b= 1
    }
    console.log(a)//1
    console.log(b)//ReferenceError: b is not defined
    
    
    // 以下代码会打印什么？
    for(var i = 0; i <= 5; i++) {

    }
    console.log(i)  // 6

    for(let j = 0; j <= 5; j++) {

    }
    console.log(j)  // ReferenceError: j is not defined
    
  
