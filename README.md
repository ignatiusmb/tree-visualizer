# Java - Tree Visualizer
A simple program to print all the nodes in the tree with a beautiful output. Connected by lines with clear paths, it's nice to look and easy to debug a tree.

## Getting Started
Download `TreeVisualizer.java` and put it in the same directory so you won't need to import anything

## How to use
1. Just put `TreeVisualizer.java` in the same directory with the `Node` file (to implement) and `Tree` file (to print)
2. Implements `Visualized` from `TreeVisualizer` to your `Node` class
3. Override `getLeft`, `getRight`, and `getValue` method with your values
```java
class Node implements TreeVisualizer.Visualized {
  Node left, right;
  String name;
  
  ...
  
  @Override
  public TreeVisualizer.Visualized getLeft() {
      return this.left;
  }

  @Override
  public TreeVisualizer.Visualized getRight() {
      return this.right;
  }

  @Override
  public String getValue() {
      return this.name;
  }
}
```
4. If your `Value` is other than a `String`, you need to modify it to return your data type
5. Use the provided `print` method and put the tree's `root` as the argument
```java
public class MyFile {
  public static void main(String[] args) {
    Tree tree = new Tree();
    TreeVisualizer.print(tree.root);
  }
}
```
**or**
```java
public class MyFile {
  public static void main(String[] args) {
    Tree tree = new Tree();
    tree.print()
  }
}

class Tree {
  Node root;
  
  ...
  
  public void print() {
    TreeVisualizer.print(this.root);
  }
}
```
## License

This project is licensed under Unlicense license - see the [LICENSE](LICENSE) file for details

---
> [imbagus.com](www.imbagus.com) &nbsp;&middot;&nbsp;
> GitHub [@ignatiusmb](https://github.com/ignatiusmb) &nbsp;&middot;&nbsp;
> GitLab [@ignatiusmb](https://gitlab.com/ignatiusmb)