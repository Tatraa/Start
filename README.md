# Start
Program, który narysuje kwadrat o zadanym boku (liczbie gwiazdek) oraz pusty w środku (też 
o zadanym boku). O parametry można zapytać w programie. 


#include <iostream>

using namespace std;

int main() {
    int wew,zew;
    int diff;
    cout<<"DLUGOSC ZEWNETRZNA KWADRATU: ";
    cin>>zew;
    while(cin.fail()) {
        cin.clear();
        cin.ignore(32767, '\n');
        cout<<"BLAD\n";
        cout<<"DLUGOSC ZEWNETRZNA KWADRATU: ";
        cin>>zew;
        
    }
    cout<<"DLUGOSC WEWNETRZNA KWADRATU: ";
    cin>>wew;
    while(cin.fail()) {
        cin.clear();
        cin.ignore(32767, '\n');
        cout<<"BLAD \n";
        cout<<"DLUGOSC WEWNETRZNA KWADRATU: ";
        cin>>wew;
        
    }
    diff=zew-wew;
    
    if(diff==0) {
        for(int g=1; g<=zew; g++) {
            for(int g=1; g<=zew; g++) {
                cout<<"* ";
            }
            cout<<endl;
        }
        return 0;
    }
    
    if(diff%2==0) {
        int width=diff/2;
        
        for(int i=1; i<=width; i++) {
            for(int j=1; j<=zew; j++) {
                cout<<"* ";
            }
            cout<<endl;

            }
            for(int f=1;f<=wew ; f++) {
                for(int i=1; i<=width; i++) {
                    cout<<"* ";
            }
            for(int j=1; j<=wew; j++) {
                cout<<"  ";
            }
            for(int i=1; i<=width; i++) {
                cout<<"* ";
        }
            cout<<endl;

        }
        for(int i=1; i<=width; i++) {
            for(int j=1; j<=zew; j++) {
                cout<<"* ";
            }
            cout<<endl;

        }
        return 0;
        
    }else{
        int newWidthOne=(diff-1)/2;
        int newWidthTwo=newWidthOne+1;
        
        for(int i=1; i<=newWidthOne; i++) {
            for(int j=1; j<=zew; j++) {
                cout<<"* ";
            }
            cout<<endl;

        }
        for(int f=1;f<=wew; f++) { 
            for(int i=1; i<=newWidthTwo; i++) {
                cout<<"* ";
            }
            for(int j=1; j<=wew; j++) {
                cout<<"  ";
            }
            for(int i=1; i<=newWidthOne; i++) {
                 cout<<"* ";
            }
            cout<<endl;
        }
        for(int i=1; i<=newWidthOne; i++) {
            for(int j=1; j<=zew; j++) {
                cout<<"* ";
            }
            cout<<endl;
        }
        return 0;

    }
}
