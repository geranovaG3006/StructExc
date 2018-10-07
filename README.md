# StructExc
Да се напише програма, която създава структура Automobile с полета brand, model, date, и price, указващи марка, модел, дата на производство и цена на автомобилите в автосалон. Да се въведе цяло число n и след него n на брой данни от тип Automobile.  Да се изведе информацията за автомобила с най-висока цена. 

#include<iostream>
using namespace std;
struct Automobile
{
       char brand [20];
       char model [20];
       char date [12];
       double price;
};
int main()
{
    int n;
    cout<<"Number of cars:";
    cin>>n;
    Automobile cars[n];
    for(int i=0;i<n;i++)
    {
            cout<<"Brand: ";
            cin>>cars[i].brand;
            cout<<"Model: ";
            cin>>cars[i].model;
            cout<<"Date: ";
            cin>>cars[i].date;
            cout<<"Price: ";
            cin>>cars[i].price;
    }
     double max_price= cars[0].price;
     int k=0;
     cout<<"Details about the most expensive car: "<<endl;
     for (int i=1;i<n;i++)
     {
         if(cars[i].price>max_price) 
         {
          max_price=cars[i].price;
          i=k;
         }
     }
          cout<<"Brand: "<<cars[k].brand<<endl;
          cout<<"Model: "<<cars[k].model<<endl;
       
       Същата задача решена чрез указател към структура:
       #include<iostream>
using namespace std;
struct Automobile
{
       char brand [20];
       char model [20];
       char date [12];
       double price;
};
int main()
{
    int n;
    cout<<"Number of cars:";
    cin>>n;
    Automobile cars[n];
    Automobile *q;
    q=cars;
    for(int i=0;i<n;i++)
    {
            cout<<"Brand: ";
            cin>>q->brand;
            cout<<"Model: ";
            cin>>q->model;
            cout<<"Date: ";
            cin>>q->date;
            cout<<"Price: ";
            cin>>q->price;
            q++;
    }
    double max_price= cars[0].price;
     int k=0;
     cout<<"Details about the most expensive car: "<<endl;
     for (int i=1;i<n;i++)
     {
         if(cars[i].price>max_price) 
         {
          max_price=cars[i].price;
          i=k;
         }
     }
          cout<<"Brand: "<<cars[k].brand<<endl;
          cout<<"Model: "<<cars[k].model<<endl;
          cout<<"Date: "<<cars[k].date<<endl;
          cout<<"Price: "<<cars[k].price<<endl;
     system("pause");
     return 0;
    }
     
     system("pause");
     return 0;
    }
          cout<<"Date: "<<cars[k].date<<endl;
          cout<<"Price: "<<cars[k].price<<endl;
     system("pause");
     return 0;
    }
     
