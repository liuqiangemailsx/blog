#TS

      /**
       *  .ts 文件生成 没有import export 会被视为一个脚本 
       *  number string boolean biglnt
       */
  
      let a: number ;
      let a: number | string; //联合类型
      a = 1;
      /**
       *  类型推断 会自动推断类型
       * 
       */
      let c: boolean = false;
      let b = false; 
      
 1.基础类型
 
       let a: string  = '';  
       let a:'';
       let a:unknown; 未知类型 类型安全到any 不可直接赋值给其他参数；
       
 2.类型断言
      
      s = e as string;  告诉解析器的实际变量
      /**
      * <类型>变量
      * 变量 as 类型
      **/
      
      s = <string>e
      
3.函数类型

      /**
      *  void;
      */
      
      let NOOP:void;
      
      function fn():void{};
      
      //never 表示永远没有返回结果
      
      function fn2() never { throw new Error('！！！！')};
      
 4.object
      
      let a : object;
      a = {};
      a = function (){};
      
      /**
      * {}表示包含哪些属性
      * ?: 可选的
      **/
      let b:{name?:string};
      
      b = {name:'孙'};
      //Property 'name' is missing in type '{}' but required in type '{ name: string; }'
      b= {}
      
      let c :{name:string,[propsName:string]:any};
      
      let b: (a:number,b:number)=>number
      
 5.array
       
       let e: string[];
       
       e = ['a','b','c'];
       
       let a: Array<number>;
      
      
      
      
      
      
      
       
       
      
      
     
      
      
      
      
      
