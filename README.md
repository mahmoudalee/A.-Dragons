# A.-Dragons

#include <iostream>

#include <algorithm>

using namespace std;

int main()
 {
 
 	int krito, n;
 	cin >> krito >> n;
 	pair<int, int> arr[10000];
 	for(int i = 0; i < n; i++)
 		cin >> arr[i].first >> arr[i].second;
 	sort(arr, arr + n);

    bool flag = false;
 	for(int i = 0; i < n; i++)
    {
        if(krito <= arr[i].first)
        {
            cout << "NO" << endl;
            flag = true;
            break;
        }
        krito += arr[i].second;
    }

    if(flag == false)
        cout << "YES" << endl;

     return 0;
 }
