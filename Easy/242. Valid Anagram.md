#题意
判断两个串是否包含的字母完全相同（只包含小写字母）

#分析
建立两个26位记录串，扫一遍记录两个串内各个字母个数，比对是否完全相同

#代码
```C++
class Solution {
public:
    bool isAnagram(string s, string t) {
        if(s.size() != t.size())
            return false;
        int i,v1[30] = {0},v2[30] = {0};
        for(i = 0;i < s.size();i ++){
            v1[s[i]-'a'] ++;
            v2[t[i]-'a'] ++;
        }
        for(i = 0;i < 26;i ++)
            if(v1[i] != v2[i])
                return false;
        return true;
    }
};
```
