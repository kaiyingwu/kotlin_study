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
   var value: Int? = null (若想为空必须在类型后加?,若真的为null则会跳过不执行，若在类型后加上!!表示该变量必不为空，若为空则给出空指针异常)
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
    
8. kotlin中若需要重写方法

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
    
11. kotlin中的for循环

    ```
    //1-10包含1和10
    for (i in 1..10) {
        if (i==3) continue  // i 为 3 时跳过当前循环，继续下一次循环
        println(i)
        if (i>5) break   // i 为 6 时 跳出循环
    }
    
    //正常循环
    for (i in 1..4) print(i) // 打印结果为: "1234"
    
    //反向循环
    for (i in 4 downTo 1) print(i) // 打印结果为: "4321"
    
    //指定步长
    for (i in 1..4 step 2) print(i) // 打印结果为: "13"
    for (i in 4 downTo 1 step 2) print(i) // 打印结果为: "42"
    
    //如果循环中不要最后一个范围区间的值可以使用 until 函数,i in [1, 10), 不包含 10
    for (i in 1 until 10) {
     println(i)
    }
    
    ```
    
    //kotlin中的switch case
    
    ```
    
    //第一种在->后直接跟上输出
    when (x) {
    0, 1 -> print("x == 0 or x == 1")
    else -> print("otherwise")
    }
    
    //第二种在->后跟上{}，输出在{}中
    when(x){
            1-> {
                println(1)
            }
            2->{
                println(2)
            }
     }
     
     //注意
    when (x) {
           1 -> print("x == 1")
           2 -> print("x == 2")
           else -> { // 注意这个块
               print("x 不是 1 ，也不是 2")
           }
    }
    
    ```
