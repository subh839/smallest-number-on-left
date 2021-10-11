# smallest-number-on-left

class Solution{
public:
    vector<int> leftSmaller(int n, int a[]){
            vector<int> ans;
        stack<int> st;
        for(int i = 0 ; i < n ; i++){
            int val = a[i];
            while(!st.empty() && st.top() >= val) st.pop();
            if(st.empty()) ans.push_back(-1);
            else ans.push_back(st.top());
            st.push(val);
        }
        return ans;
    
    }
};
