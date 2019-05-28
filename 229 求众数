//摩尔投票法
class Solution {
public:
    vector<int> majorityElement(vector<int>& nums) {
        vector <int> result;
        int m1=0,m2=0;
        int cnt1=0,cnt2=0;
        for(int i=0;i<nums.size();i++){//选出出现最多的两个数，并且避免两个数相同
            if(m1==nums[i] && cnt1!=0){
                cnt1++;
            }else if(m2==nums[i] && cnt2!=0){
                cnt2++;
            }else if(cnt1==0){
                m1=nums[i];
                cnt1++;
            }else if(cnt2==0){
                m2=nums[i];
                cnt2++;
            }
            else {
                cnt1--;
                cnt2--;
            }           
            
        }
        cnt1=0;
        cnt2=0;
        //重新计算两个数出现的次数，有可能正好等于n/3 or 在上轮迭代快结束的时候正好被赋给m1 or m2
        for(int i=0;i<nums.size();i++){
            if(m1==nums[i]){
                cnt1++;
            }else if(m2==nums[i]){
                cnt2++;
            }
        }
        int size=floor(nums.size()/3);
        if(cnt1>size){
            result.push_back(m1);
        }
        if(cnt2>size ){
            result.push_back(m2);
        }
        return result;
        
        
    }
};
