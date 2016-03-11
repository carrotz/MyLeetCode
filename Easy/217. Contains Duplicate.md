#题意
检测数组里是否有重复值

#分析
排序、检查每一项是否与前一项相同

#代码
```C++
class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        sort(nums.begin(), nums.end(),less<int>());
        for(int i = 1;i < nums.size();i ++)
            if(nums[i] == nums[i-1])
                return true;
        return false;
    }
};
```
