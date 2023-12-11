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
