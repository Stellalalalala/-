# 高二資訊科技課堂作業

## Unit 1 程式語言介紹
### 1.Hello World
"Hello world!"一支最基礎的程式，一句來自電腦世界的問候，同時也是許多人接觸到的第一個範例程式。

請輸出 Hello world!

    #include <iostream>
    using namespace std ;

    int main()
    {
        cout << "Hello world!" << endl ;
    }

## Unit 2 變數運算與輸入輸出

### 2.BMI 計算機
BMI 公式為 體重/(身高*身高公尺)，

請撰寫程式，輸入姓名、身高公分、體重後，輸出歡迎訊息和 BMI 值
   
    #include <iostream>
    using namespace std;

    int main()
    {
        string name;
        double h, w;

        cin >> name;

        cin >> h >> w;
        h = h / 100;

        cout << "哈囉 " << name << " =w=" << endl;
        cout << "你的 BMI 是 " << w / (h*h) << endl;
    }
    
## Unit 3 流程控制(IF)
### 3-1.BMI 計算機(續)
BMI 公式為 體重/(身高*身高公尺)，

請嘗試修改上一份程式，輸入身高公分、體重後，輸出 BMI 值和分級訊息

（<18.5：過輕 / 18.5-24.9：標準 / 25-29.9：過重 / 30-34.9：中度肥胖 / 35< ：嚴重肥胖）

    #include <iostream>
    using namespace std;

    int main()
    {
        double H , W, BMI;
        cin >> H >> W;

        H = H / 100;
        BMI = W / (H * H);

        cout << "你的 BMI 是 " << BMI << endl ;

        if(BMI < 18.5)
        {
            cout << "BMI 過輕" << endl;
        }
        else if(18.5 <= BMI && BMI <= 24.9)
        {
            cout << "BMI 標準" << endl;
        }
         else if(25 <= BMI && BMI <= 29.9)
        {
            cout << "BMI 過重" << endl;
        }
         else if(30 <= BMI && BMI <= 34.9)
        {
            cout << "BMI 中度肥胖" << endl;
        }
        else
        {
            cout << "BMI 嚴重肥胖" << endl;
        }
    }
### 3-2.HGSH online
Hungry Girl Say High(簡稱：HGSH) 是一款新型線上遊戲。

在遊戲中每個玩家都會有一個編號，以對應初始飢餓值。

編號 5 的倍數	初始飢餓值：500

編號 2 的倍數	初始飢餓值：200

其他	初始飢餓值：50

如果同時符合多個時，因為人總是飢餓的，所以要取飢餓值較大者。

另外因為近年食物短缺，如果是後加入者，也就是編號超過 123 時，飢餓值要再加上 100。

◆輸入說明：一個整數，即玩家編號

◆輸出說明：一個整數，即對應飢餓值(結尾需換行)

    #include <iostream>
    using namespace std;

    int main()
    {
        int n , hungry = 0;
        cin >> n;

        if( n % 5 == 0)
        {
            hungry = hungry + 500;
        }
        else if( n % 2 == 0)
        {
            hungry = hungry + 200;
        }
        else
        {
            hungry = 50;
        }

        if( n > 123 )
        {
            hungry = hungry + 100;
        }

        cout << hungry << endl;
    }



