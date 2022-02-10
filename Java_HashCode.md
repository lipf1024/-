## String

```java
   public int hashCode() {
        int h = hash;
        if (h == 0 && value.length > 0) {
            char val[] = value;

            for (int i = 0; i < value.length; i++) {
                h = 31 * h + val[i];
            }
            hash = h;
        }
        return h;
    }
```
相同字符串得到的Hash值应该是相同的

####Hash碰撞
int型的值取值范围为Integer.MIN_VALUE(-2147483648)～Integer.MAX_VALUE(2147483647)，所以如果字符串比较长，计算的数值就可能超出Integer.MAX_VALUE，造成数值溢出，值变成负数
产生碰撞的原因：
 1. hashCode使用不同的算法产生碰撞不可避免
 2. int值的限制
