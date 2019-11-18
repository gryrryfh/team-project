## 유튜브 링크 : https://www.youtube.com/watch?v=pShZ2umGXU8
## 소스코드
```
#include <stdio.h>
 
void swap(int* a, int* b) {
    int t = *a;
    *a = *b;
    *b = t;
}
 
 
void quickSort(int left,int right, int* data) {
    int pivot = left;
    int j = pivot;
    int i = left+1;
 
    if (left < right) {
        for (; i <= right; i++) {
            if (data[i] < data[pivot]) {
                j++;
                swap(&data[j], &data[i]);
            }
        }
        swap(&data[left],&data[j]);
        pivot = j;
 
        quickSort(left, pivot-1,data);
        quickSort(pivot+1, right, data);
    }
 
}
 
int main() {
 
    int arr[5] = { 5,4,3,2,1 };
    int i;
    quickSort(0, 4, arr);
    for (0; i < 5; i++) printf("%d ",arr[i]);
 
    return 0;
}
```
