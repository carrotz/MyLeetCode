#题意
给出excel表格列编码，计算是第几列

#分析
类似16进制转10进制算法，模拟累加即可

#代码
```C++
class Solution {
public:
    int titleToNumber(string s) {
        int res = 0,i,tmp = 1;
        for(i = s.size()-1;i >= 0;i --){
            res += ((s[i]-'A')+1)*tmp;
            tmp *= 26;
        }
        return res;
    }
};
```
