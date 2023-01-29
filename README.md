//Ada and Queue 
// by abdulaziz alghoribi 

#include <bits/stdc++.h>

using namespace std;
#define abdulaziz ios::sync_with_stdio(false);cin.tie(NULL);cout.tie(NULL);

int main()
{

    abdulaziz
    int q, f=1;
    unsigned short n;
    string s;

    deque <int> dq;
    cin >> q;
    for(int j = 0; j < q ; j++)
    {
        cin >> s;
        //print back
        if(s == "back")
        {
          if(dq.empty()){
            cout<<"No job for Ada?"<<endl;
          }
          else if (f%2 != 0){
            cout << dq.back() << endl;
            dq.pop_back();
          }
          else{
           cout << dq.front() << endl;
           dq.pop_front();
          }
        }

        // print front
        else if(s == "front")
        {
          if(dq.empty()==1){
            cout << "No job for Ada?" <<endl;
          }
          else if (f%2 != 0){
            cout << dq.front() << endl;
            dq.pop_front();
          }
          else{
           cout << dq.back() << endl;
           dq.pop_back();
          }
        }
        //reverse
        else if (s == "reverse")
        {
          f++;
        }
        //push front
        else if (s == "toFront")
        {
          cin >> n;
          if(f%2 != 0)
            dq.push_front(n);
          else
            dq.push_back(n);
        }

        //push back
        else if (s == "push_back") 
        {
          cin >> n;
          if(f%2 != 0)
            dq.push_back(n);
          else
            dq.push_front(n);
        }
        //loop
    }
    return 0;
}
