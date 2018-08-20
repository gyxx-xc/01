# 01

```c++
#include <bits/stdc++.h>
using namespace std;

int a[1005];

int main(){
	freopen("diamond.in", "r", stdin);             
	freopen("diamond.out", "w", stdout);           
	int n, ans = 0, Max, Min, temp, k;             
	scanf("%d%d", &n, &k);                         
	for(int i = 0; i < n; i ++){                   
		scanf("%d", &a[i]);                        
	}                                              
	for(int j = 0; j < n; j ++){                   
		temp = 1;                                  
		Min = a[j];                                
		Max = a[j];                                
		for(int i = j+1; i < n; i ++){             
			if(Max - k <= a[i] && a[i] <= Min + k){
				Min = min(Min, a[i]);
				Max = max(Max, a[i]);
				temp ++;
			}
		}
		ans = max(temp, ans);
	}
	printf("%d\n", ans);
}
```
