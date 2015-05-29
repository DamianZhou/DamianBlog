---
title: Code Syntax
---
To insert highlight code inside of a post, it's enough to use some specific tags, has directly described into the [Jekyll documentation](http://jekyllrb.com/docs/templates/#code-snippet-highlighting). In this way the code will be included into a ``.highlight`` CSS class and will be highlight according to the [syntax.scss](https://github.com/mojombo/tpw/blob/master/css/syntax.css) file. This is the standard style adopted by **Github** to highlight the code. 

This is a CSS example:
{% highlight css linenos %}

body {
  background-color: #fff;
  }

h1 {
  color: #ffaa33;
  font-size: 1.5em;
  }

{% endhighlight %}

And this is a HTML example, with a linenumber:
{% highlight html linenos %}

<html>
  <a href="example.com">Example</a>
</html>

{% endhighlight %}

Last, a Ruby example:
{% highlight ruby linenos %}

def hello
  puts "Hello World!"
end

{% endhighlight %}


测试一下别的语法：

```bash
netstat -lnp
```

Java的

```java
public class PriorityQueueDemo {
  
  void minKDemo(){
    
    PriorityQueue<Integer> heap = new PriorityQueue<>(4, new Comparator<Integer>() {

      @Override
      public int compare(Integer o1, Integer o2) { 
        return o1-o2;   //小的在前
      }
    });
    
    int[] nums = {3,6,8,9,1,4,17,67};
    for(int a : nums){
      heap.add(a);
    }
    
    System.out.println(heap.peek());
    System.out.println(heap.size());
    System.out.println(Arrays.toString(heap.toArray()));
  }

  public static void main(String[] args) {
    PriorityQueueDemo test = new PriorityQueueDemo();
    test.minKDemo();

  }

}
```
