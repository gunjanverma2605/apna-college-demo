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
class Solution {
  public:
    bool isSorted(vector<int>& arr) {
         for(int i=1;i<arr.size();i++){
            if(arr[i-1]>arr[i]){
                return false;
            }
        }
        return true;
    }
};

One more method
class Solution {
  public:
    bool isSorted(vector<int>& arr) {
        for(int i=0;i<arr.size()-1;i++){
            if(arr[i]>arr[i+1]){
                return false;
            }
        }
        return true;
    }
};

4.Remove duplicates from Sorted Array
class Solution {
  public:
    vector<int> removeDuplicates(vector<int> &arr) {
        int i=0;
        for(int j=1;j<arr.size();j++){
            if(arr[i]!=arr[j]){
                i++;
                arr[i]=arr[j];
            }
        }
        arr.resize(i+1);
        return arr;
    }
};

5.Left Rotate an array by one place
class Solution {
  public:
    void rotate(vector<int> &arr) {
        int first = arr[0];
        for(int i = 1; i < arr.size(); i++) {
            arr[i-1] = arr[i];
        }
        arr[n-1] = first;
    }
};

6.Left Rotate an array by D places(Reversal Algorithm)
class Solution {
  public:
    void leftRotate(vector<int>& arr, int d) {
        int n=arr.size();
        d%=n;
        reverse(arr.begin(),arr.begin()+d);
        reverse(arr.begin()+d,arr.end());
        reverse(arr.begin(),arr.end());
    }
};

7.Move Zeors to End
class Solution {
  public:
    void pushZerosToEnd(vector<int>& arr) {
        int i=0;
        for(int j=0;j<arr.size();j++){
            if(arr[j]!=0){
                swap(arr[i],arr[j]);
                i++;
            }
        }
    }
};

8.Linear Search





