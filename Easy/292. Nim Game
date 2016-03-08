#题意
一堆石子有n个，每次可以取1-3个，最后一个取完获胜，问先手是否能获胜

#分析
必胜：1,2,3,5,6,7,9,10,11……
必败：4,8,12……
策略：可以被4整除的必败

#代码
``` 
   
class Solution {
public:
    bool canWinNim(int n) {
        return (n % 4) ? true : false;
    }
};
   
```
