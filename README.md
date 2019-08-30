# program-6
6. Remove Friends
After getting her PhD, Christie has become a celebrity at her university, and her
Facebook profile is full of friend requests. Being the nice girl, she is, Christie has
accepted all the requests.
Now Kuldeep is jealous of all the attention she is getting from other guys, so he asks
her to delete some of the guys from her friend list.
To avoid a 'scene', Christie decides to remove some friends from her friend list, since
she knows the popularity of each of the friend she has, she uses the following
algorithm to delete a friend.


#include<iostream>
#include<vector>
using namespace std;
int main()
{
int t;
cin>>t;
while(t--)
{
int n,k,x=0;
cin>>n>>k;
vector<int> stck;
while(n--)
{
int y;
cin>>y;
while(!stck.empty()&&x<k&&stck.back()<y)
{
stck.pop_back();
x++;
}
stck.push_back(y);
}
while(x<k)
{
stck.pop_back();
x++;
}
for(int i=0;i<stck.size();i++)
cout<<stck[i]<<" ";
cout<<endl;
}
}
