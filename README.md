# java_method
## javaのメソッドについてまとめていく。
### メソッドとは
何らかの処理を割り当てた部品。  
Javaのファイルを実行すると、自動的にmainメソッドが実行される。  
mainメソッドの処理をメソッドに切り分けると、mainメソッドが各メソッドに指示を出し、  
各メソッドが個々の処理を実行するという構造になる。  
メソッドにはインスタンスメソッドとクラスメソッドと呼ばれるものがある。  

### メソッドの定義
メソッド名は好きに付けることができるが、処理の内容が想像できるような名前をつける。  
メソッドはクラスの中に定義する。クラス中に定義しないとエラーになるため、気をつける。  
メソッドを呼び出すためには、メソッド名()とするだけ。  
呼び出しの時の()を忘れない。  
例  
```
class Main {
  public static void main(String[] args) {
    printData();
    
  }
  
  public static void printData() {
    System.out.println("私の名前はJon Smithです");
  }
  
}
```
  
### 引数
メソッドに引数を渡すには、まず引数を受け取れるメソッドを定義する必要がある。  
そのためにはメソッドの定義部分で、引数を受け取るための箱となる変数（仮引数（かりひきすう））を指定する。  
例として「public static void メソッド名()」の()に仮引数を指定。仮引数は、変数定義と同様に、データ型を指定する必要がある。  
メソッドに引数を渡すには、メソッド名(引数)としてメソッドを呼び出す。  
渡された引数は、メソッドの仮引数で指定した変数に代入され、その変数はメソッドの処理の中で用いることができる。  
例  
```
class Main {
  public static void main(String[] args) {
    printData("Kate Jones");
    
  }

  public static void printData(String name) {
    System.out.println("私の名前は" + name + "です");
    
  }
}
```
出力結果 ： 私の名前はKate Jonesです  

引数は複数渡すことも可能。メソッドが複数の引数を受け取るためには、仮引数をコンマ（,）で区切って定義する。  
また、引数は左から順番に「第1引数、第2引数・・・」というように呼ぶ。
```
class Main {
  public static void main(String[] args) {
    printData("John Christopher Smith", 65);
  }

  public static void printData(String name, int age) {
    System.out.println("私の名前は" + name + "です");
    System.out.println("年齢は" + age + "歳です");
    
  }
}
```
出力結果  
私の名前はJohn Christopher Smithです  
年齢は 65歳です
