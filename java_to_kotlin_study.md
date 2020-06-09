# java中的各类命名变化

1. private
   
   kotlin中未变化还是private的命名方法
   
2. public
   
   kotlin中变化成open

3. 常量变量的命名方式的改变

   kotlin中命名例子
   ```
   
   var 变量名: 变量类型 = 类名()   或
   var 变量名: 类名()            或
   var 变量名: 变量类型？ = null  或
   lateinit var 变量名: 变量类型
   如：
   var value: Int = 1 或
   var value = 1 或
   var value: Int? = null (若想为空必须在类型后加?)
   lateinit var value: A  //A为非基础类型的类
   val与var类似，只是定义后无法再更改它的数据
   
   ```
   
4. 公共参数的定义即java中的 static final

   ```

   companion object {
         //公共参数的定义
         const val appKey : String = ""
         const val secretKey: String = ""
         //公共方法的定义
         fun get（）{
         
         }
    }

    ```

5. java中的类定义，并且实现继承（extends），以下为kotlin中的例子
 
    ```

    class MyActivity : AppCompatActivity(){
    //extends 用：代替后面跟需要继承的类

    }
  
    ```

6. java中方法的定义，以下为kotlin中的例子
    
    ```

    //无返回参数的情况下
    fun get(){

    }

    //需要返回参数的情况下
    fun get() : Int{
    return 0
    }

    ```
    
7.  java中字符串与数字之间的拼接，以下为kotlin中的例子

    ```
    
    "字符串$数字"
    "qwer$1"
    
    ```
    
8. kotlin中若需要重现方法

    ```
    
    override fun get(){
     //重写方法需要加上override 一般情况下工具会默认加上
    }
    
    ```
    
9. java中的implement，以下为kotlin中的例子

    ```
    
    class MyActivity : AppCompatActivity(),View.OnClickListener{
    //用，来代替implement
    }
    
    ```
    
10. kotlin 中的强转

    ```
    
     private var str : String = "1"
     var x = str.toInt()
     
     //常用的强转类型
     //toByte(): Byte
     //toShort(): Short
     //toInt(): Int
     //toLong(): Long
     //toFloat(): Float
     //toDouble(): Double
     //toChar(): Char
    
    ```
    
