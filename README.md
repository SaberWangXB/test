# test
#include "stdafx.h"
#include <iostream>  
#include <list>  
#include <vector>  
#include <deque>  
#include <set>  
using namespace std; 

int _tmain(int argc, _TCHAR* argv[])
{
	vector<int> v;  
	v.insert(v.begin(),1);  //如果使用insert(1)不指定插入位置，会出错  
	v.insert(v.begin(),2);  
	v.insert(v.begin(),1);  
	v.insert(v.begin(),3);  
	vector<int>::iterator vp = v.begin();  
	for(vp = v.begin();vp < v.end(); vp++)  
		cout << *vp << endl;  

	set<int> a (v.begin(), v.end());
	set<int>::iterator ap = a.begin(); 
	while(ap != a.end())  
		cout << *ap++ << endl;

	set<int> s;  
	s.insert(s.begin(),1);  
	s.insert(s.begin(),2);  
	s.insert(s.begin(),10);
	s.insert(s.begin(),1);  
	s.insert(s.begin(),3); 
	set<int>::iterator sp = s.begin();  //for(vp = v.begin();vp < v.end(); vp++)  //如果使用这句会出错，因为set容器对<没有重载  
	 while(sp != s.end())  
		cout << *sp++ << endl;  
	return 0;  
}
