## template

```cpp
#include <bits/stdc++.h>
using namespace std; 
using ll = long long;

int main() {
}  
```

## 変数の宣言

```cpp
int a;//整数(32bit,およそ10^9以下にしか使わない)
ll b;//整数(64bit,全部これでok)
double d;//小数
string s;//文字列
char c;//文字(1文字)
```

```cpp
//このように宣言しても良い
int a=3;
ll b=100000000000;
double d=0.5;
string s="abcde"
char c='c'
```

## 配列
```cpp
vector<int> v(5);//長さ5のintの配列ができる
vector<int> v2(100,3);//長さ100のintの配列ができる、中身はすべて0になる
vector<string> v3(20);//長さ20のstringの配列ができる

v[0]=1;//0番目から始まるので注意
v[1]=2;
v[2]=3;

//v[5]=10;　これはエラーになる。配列の長さは5なので、0番目から4番目までしかない
```

## 入力と出力

```cpp
cout << 1 << endl;
cout << "Yes" << endl;//文字列は""必須

int a;
cin >> a;
cout << a << endl;

string b,c;
cin >> b >> c;//複数入力することもできる
cout << a << " " << b << " " << c << endl;//複数出力するときはスペースが必要

vector<int> v(10);
v[0]=1;
```



## if文
```cpp
int a=5,b=3;
if(a>b){
  //５は3より大きいので、実行される
}
else{
  //ifの中身が実行されたので、実行されない
}

int c=8;

if(a<=b){
  //a<=bではないので実行されない
}
else if(b<=c){
  //前のif文は実行されなくて、b<=cなので実行される
}
else if(a<=c){
  //前のif文は実行されたので、a<=cだが実行されない
}

```

| 記号 | 意味 |
| ---- | ---- |
| a < b | aはbより小さい |
| a > b | aはbより大きい |
| a <= b | aはb以下 |
| a >= b | aはb以上 |
| a == b | aとbは等しい |
| a != b | aとbは等しくない |
| <条件式1> && <条件式2> | 条件式1 かつ 条件式2 |
| <条件式1> \|\| <条件式2> | 条件式1 または 条件式2 |


## ループ
```cpp
for(int i=0;i<n;i++){
  //ここに実行したいコードを書く(n回実行される)
}

while(/*条件式*/){
  //ここに実行したいコードを書く(条件式が満たされなくなるまで)
}
```

## 関数
一部しか載せないので、気になったら調べること
```cpp
cout << max(3,5) << endl;//5
cout << min(2,4) << endl;//4

vector<int> v={4,2,3};
sort(vec.begin(),vec.end());//
cout << v[0] << " " <<  v[1] << " " << v[2] << endl;//2 3 4
reverse(vec.begin(),vec.end());
cout << v[0] << " " <<  v[1] << " " << v[2] << endl;//4 3 2
```

## コードの例
複数個の整数の入力を受け取るとき
```
5
3 1 4 1 5
```
```cpp
#include <bits/stdc++.h>
using namespace std; 
using ll = long long;

int main() {
  int n;
  cin >> n;
  vector<int> v(n);

  for(int i=0;i<n;i++){
    cin >> v[i];
  }
}  
```

## 実行
a.cppというファイルを実行したいとき
```
g++ a.cpp
./a.exe
```


## トラブルシューティング
- ;(セミコロン)を忘れていないか
- 同じ変数名を2回宣言していないか
- "Yes","No"を"yes","no"としていないか
- オーバーフローしていないか → intでなくllを使えば解決するかも
- コードを書き換えたあと、g++ *.cppを忘れていないか



