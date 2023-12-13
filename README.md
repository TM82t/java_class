# java_class
## Javaのクラスについてまとめていく。
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

### ライブラリ
Javaでは他者が作ったクラスを利用することが可能。このようなクラスを外部ライブラリと呼び、自分のプログラムに読み込むことで利用できるようになる。  
すべてのプログラムを自分だけで開発する必要は無く、世界中のエンジニアが作った便利なメソッドを利用することで開発の幅は一気に広がる。  
外部ライブラリを自分のプログラムに読み込む（使えるようにする）には、importを用いる。  
クラス（ライブラリ）を読み込むにはclass定義より上で「import java.lang.〇〇」とする。  
例
```
import java.lang.〇〇;

class Main {
  public class static void main(String[] args {
  ・
  ・
  ・
 }
}
```
java.langパッケージはJavaの基本的な機能がまとめられたパッケージ。  
頻繁に利用するので「コンパイラが勝手にimportをしてくれる仕組み」になっている。
そのため、インポート宣言をする必要が無い。また、同じパッケージに属するクラスのインポート宣言も省略が可能。
また、インポート宣言時にアスタリスクを使って、そのパッケージに属するすべてのクラスをインポートが可能。
System、String、StringBuffer、StringBuilder、Boolean、Byte、Integer、Mathなど  
様々なクラスがjava.langには用意されている。  
  
### 入力の受け取り
コンソールに値を「入力」し、その値をプログラム内で使うこともできる。
コンソールへの入力を受け取るには「Scanner」というライブラリを用いる。  
Scannerは「import java.util.Scanner」と読み込む。  
例
```
import java.util.Scanner;

class Main {
  public static void main (String[] args) {
    Scanner scanner = new Scanner(System.in);
    
    System.out.print("名前： ");

    String name = scanner.next();

    System.out.println("こんにちは" + name + "さん");
  }
}
```
Scannerを用いて整数を受け取るメソッドはnextIntメソッド、小数を受け取るメソッドはnextDoubleメソッドを使用。
