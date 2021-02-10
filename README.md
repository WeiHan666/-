# 算法编程笔记

编程题目心得


1，重载运算符<
  在std::map里面，需要重载自定义结构体的<运算符。而两个自定义结构体相等的判断，同样需要<运算符。当两个结构体的<运算符，在交换位置后，返回结果还是都为false，就认为两个结构体相等。
  struct Point{
      int x;
      int y;
      bool operator <(const Point other) const{
          if(x!=other.x){
              x<other.x;
          }
          if(y!=other.y){
              y<other.y;
          }
          return false;
      }
  };
