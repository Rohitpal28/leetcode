class Solution {
public:
    int search(vector<int>& arr, int tar) {
     sort(arr.begin(),arr.end());
      int st=0;
      int n=arr.size();
      int end=n-1;
        while(st<=end){
          int  mid=(st+end)/2;
            if(tar>arr[mid]){
                st=mid+1;
            }
            else if(tar<arr[mid]){
                end=mid-1;
            }
            else{
                return mid;
            }
        }
        return -1;
    }
};
