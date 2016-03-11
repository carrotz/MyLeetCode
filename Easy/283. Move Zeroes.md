#题意
把数组里的0移动到最后面

#分析
扫一遍记录非零值，重构数组，后面补0

#代码
```C++
class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        int i;
        vector<int> nozero;
        for(i = 0;i < nums.size();i ++)
            if(nums[i] != 0)
                nozero.push_back(nums[i]);
        for(i = 0;i < nozero.size();i ++)
            nums[i] = nozero[i];
        for(i = nozero.size();i < nums.size();i ++)
            nums[i] = 0; 
    }
};
```
