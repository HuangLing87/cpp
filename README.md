指標
=====

指標是存儲變數內存地址的變量  
使用&取地址運算符獲取變量地址   
使用*解參考運算符獲取指針所指向的值 
	
		int x = 10;  
		int *ptr = &x; // ptr存儲x的內存地址  
		cout << ptr << endl; // 輸出x的地址  
		cout << *ptr << endl; // 輸出x的值10  

指標運算
-------

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
=======

矩陣-一維陣列
-------

		int arr[5]; // 宣告長度為5的整數陣列  
		int arr[] = {1, 2, 3, 4, 5}; // 初始化陣列  
		int *ptr = arr; // 將指標指向陣列的首位址  

矩陣-二維陣列
-------

		int arr[3][4]; // 宣告3x4的二維整數陣列,所有元素默認初始化為0  
		int arr[2][2] = {{1, 2}, {3, 4}}; // 初始化二維陣列  
		int (*ptr)[4] = arr; // 將指標指向二維陣列的首位址  

矩陣-多維陣列
-------

三維陣列可視為一維陣列,其元素為二維陣列  
高維陣列的宣告與存取方式類似  

		int arr[2][3][4]; // 宣告2x3x4的三維整數陣列  
		arr[0][1][2] = 10; // 存取第1個二維陣列中的第2行第3個元素  
			for (int i = 0; i < 2; i++) {  
				for (int j = 0; j < 3; j++) {  
					for (int k = 0; k < 4; k++) {  
						cout << arr[i][j][k] << " "; // 按維度順序遍歷輸出元素  
					}  
				cout << endl;  
				}  
				cout << endl;  
			}  

標頭檔
=======
需儲存附檔名為.h，且在主程式中需#include "[標頭檔檔名].h"

頭文件保護
-------
頭文件保護是通過預處理指令 #ifndef，#define，#endif 實現的，防止同一個頭文件被多次包含。

		#ifndef HEADER_FILE_NAME_H
		#define HEADER_FILE_NAME_H
		
		// 頭文件內容
		
		#endif // HEADER_FILE_NAME_H
