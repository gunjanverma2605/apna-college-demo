#ARRAYS

1.Largest Element in an Array
class Solution {
  public:
    int largest(vector<int> &arr) {
        int max=arr[0];
        for(int i=1;i<arr.size();i++){
            if(arr[i]>max){
                max=arr[i];
            }
        }
        return max;
    }
};

2.Second Largest Element in an Array without sorting
class Solution {
  public:
    int getSecondLargest(vector<int> &arr) {
        int first=-1,sec=-1;
        for(int i=0;i<arr.size();i++){
            if(arr[i]>first){
                sec=first;
                first=arr[i];
            }
            else if(arr[i]>sec && arr[i]!=first){
                sec=arr[i];
            }
        }
        return sec;
    }
};

3.Check if the array is Sorted


