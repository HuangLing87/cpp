指標

指標是存儲變數內存地址的變量  
使用&取地址運算符獲取變量地址   
使用*解參考運算符獲取指針所指向的值 

例:  
int x = 10;  
int *ptr = &x; // ptr存儲x的內存地址  
cout << ptr << endl; // 輸出x的地址  
cout << *ptr << endl; // 輸出x的值10  

指標運算

可對指針進行遞增/遞減運算,指向下/上一個元素  
指針相減得到元素個數  
指針與整數相加/相減可獲得新的地址  

int arr[] = {1, 2, 3, 4, 5};  
int *ptr = arr;   // ptr指向arr第一個元素  
cout << *ptr << endl;   // 輸出1  
ptr++;   // ptr指向下一個元素  
cout << *ptr << endl;   // 輸出2  
int *end = arr + 5;     // end指向arr最後一個元素後的地址  
int size = end - arr;   // size = 5  

矩陣

