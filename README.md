# java_class
### 他クラスのメソッドの呼び出し  
クラスは、メソッドという小さな部品をまとめるより大きな部品。  
mainメソッドと同じクラス（Mainクラス）のメソッドを使えるが、他のクラスのメソッドを利用することも可能。  
下の例ではMainクラスとPersonクラスの2つのクラスがあり、MainクラスのmainメソッドでPerson.hello()としている。    
このようにクラス名.メソッド名()とすることで、他のクラスのメソッドを呼び出すことができる。  
例  
Main.java
```
class Main {
  public static void main(String[] args) {
    Person.hello();
  }
}
```
  
Person.java
```
class Person {
  public static void hello() {
    System.out.println("Hello Java");
  }
}
```

### クラスの定義  
クラスの定義は「class クラス名」。  
また、クラス名の最初の文字は大文字、ファイル名は「クラス名.java」とする必要がある。  
クラスを分割することで実行用のクラス、ロジックをまとめるクラスという役割分担が明確になる。  
Javaはファイルではなくクラスを実行する。  
また、実行時にmainメソッドが呼ばれるが、正確にはmainメソッドを持つクラスしか実行できない（mainメソッドのないクラスは他クラスから呼び出して使う）。  
またクラス名に関係なく、実行時にはmainメソッドが呼ばれる（Mainクラスだからmainメソッドが呼ばれるというわけではない）。  
