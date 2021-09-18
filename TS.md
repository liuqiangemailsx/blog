#TS

   TS是什么
   
        它是 JavaScript 的一个超集，而且本质上向这个语言添加了可选的静态类型和基于类的面向对象编程;
    
    流程
    
        TS ---> JS ----> 打包 ---->发布
      
  




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
       let count:number = '';
       let isDone:boolean =false;
       let sym:Symbol()
       let arr:Array = [];
       let arr:Array<number | string> = [];
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
  
 6.元组 tuple
       /***
       * 元组就是已知的参数声明;
       **/
 
       let h:[string,number]
        h = ['a',1];
        
 7.enum 枚举
 
        /**
        *   enum默认从0 开始也可以字符串开始进行枚举， 还支持反向映射. 常量枚举. 异构枚举
        *   
        */
        
        enum InputProps {
             lang = 'lg',
             samll = 'sm'
        }
        InputProps['lg'] //lang
        INputProps['lnag']//lg
        
        let num = InputProps.lang
        
        const enum Props{
            NOOP,
        }
        
        enum InputProps{
            A,
            B,
            C = 'c',
            D = 'd'
        }
        
        InputProps.A // 0
             
             
        
 8.interface type
 
         interface InputProps {
              name:string,
              age?:number,
              sex:number,
          }
          
          type a  = string | number;
          
          function fn<T>(name: T, sex: T) {
           }
            fn<string>('112', '222')
            
  9.declare 
  
            declare function fn(){};
        
  10.keyof
  
            type Preson = {
              name: string,
              age:number,
            }
            
            type PresonKey = keyof Preson;
            
   11 Any 类型
   
            ts中任何类型都可以规为any类型，为所有类型的顶级类型。
            
             let notSoure:any = '1';
             notSoure = false,
             notSoure = 1;
             
   12.unknown;
   
            新更新的类型，跟any是一样，所有的类型都可以进行unknown,只可以any或者unknown 进行赋值， 其他类型会报错
            
            
            let value:unknown;
            
            value = false;
            value = 1;
            
            
            let value1:string = value //error
            
            
            
    13.void 
    
    
           void 表示是没有任何类型，跟any相反，一般用于函数返回, 严格模式是undefined
           
           
           function fn():void {
           
           }
           
    14. null - undefined
   
            let u: undefined = undefined;
            let n: null = null;
    
    15.object 
    
             let a:object | null 
             
     16.
             
            
            
            
      
       
      
      
      
      
      
      
       
       
      
      
     
      
      
      
      
      
