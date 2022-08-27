#include<iostream>
using namespace std;

void merge_sort(int* array, int begin, int end);
void divide(int* array, int begin, int end);
void merge(int* array,int begin, int mid, int end);

int main(){
    int n;
    cin >> n;
    int array[n];
    int i = 0;
    while(i != n){
        cin >> array[i];
        i++;
    }
    merge_sort(array, 0, n-1);
    for(i=0; i<n; i++)   cout << array[i] << " ";
    return 0;
}

void merge_sort(int* array, int begin, int end){
    divide(array, begin, end);
}

void divide(int* array, int begin, int end){
    if(begin==end){
        return;
    }
    int mid = begin+(end-begin)/2;
    divide(array, begin, mid);
    divide(array, mid+1, end);
    merge(array,begin,mid,end);
}

void merge(int* array,int begin, int mid, int end){
    int left_array_size = mid-begin+1;
    int right_array_size = end-mid;
    int* left_array = new int[left_array_size];
    int* right_array = new int[right_array_size];
    int left_array_index = 0, right_array_index = 0;
    int array_index = begin;
    for(int i=0; i<left_array_size; i++){
        left_array[i] = array[begin];
        begin++;
    }
    mid++;
    for(int i=0; i<right_array_size; i++){
        right_array[i] = array[mid];
        mid++;
    }
while(left_array_index != left_array_size && right_array_index != right_array_size){
    if(left_array[left_array_index] <= right_array[right_array_index]){
        array[array_index] = left_array[left_array_index];
        left_array_index++;
        array_index++;
    }
    else{
        array[array_index] = right_array[right_array_index];
        right_array_index++;
        array_index++;
    }

}
while(right_array_index != right_array_size){
    array[array_index] = right_array[right_array_index];
    right_array_index++;
    array_index++;
}
while(left_array_index != left_array_size){
    array[array_index] = left_array[left_array_index];
    left_array_index++;
    array_index++;
}
}
