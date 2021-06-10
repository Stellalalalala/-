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

## Unit 4 迴圈(for)
### 4-1. 巴斯光年
「飛向宇宙，浩瀚無垠！(To Infinity and Beyond)」

身為一個星際太空人玩具，巴斯光年決定完成他的使命：「飛向宇宙」
請寫一個程式，幫助他做發射秒數的倒數計時

◆輸入說明：一個正整數，代表倒數總秒數

◆輸出說明：秒數倒數過程，結尾需換行

    #include <iostream>
    using namespace std;

    int main()
    {
        int N;
        cin >> N;

        for(int i = N ; i >= 1 ; --i )
        {
            cout << i << " ..." << endl;
        }

        cout << "飛向宇宙，浩瀚無垠！" << endl;

    }

# 4-2.雙11購物節
11月11日是「雙 11 購物節」，這天所有東西都會打折

已知每個客人都恰好買三件商品，分別為 A、B、C

給定 N 個客人所買的三件商品價錢，和加總後需打折數 K，求商品最後總和

◆輸入說明：第一行為正整數 N，代表接下來有 N 組測資。每組皆有四個數字，分別為三個正整數代表商品價錢 A、B、C，和一個小數代表打折數 K

◆輸出說明：計算打折後商品總和

    #include <iostream>
    using namespace std;

    int main()
    {
        int N;
        cin >> N;

        for (int i = 0; i < N ; ++i)
        {
            double a,b,c,k;
            cin >> a >> b >> c >> k ;
            cout << (a+b+c) * k << endl;
        }
    }

# 4-3.七公斤魔咒
在 HGSH online 中謠傳有「七公斤魔咒」，可怕的是隨著時間，魔咒已經由最初登出會較登入增加七公斤轉變為「每待在遊戲中一年，就會增加七公斤」

假設每個玩家都會在遊戲中待滿三年，給定 N 個玩家所在年級 Y 和該年級初始體重 W，求最後登出時體重

◆輸入說明：第一行為正整數 N，代表接下來有 N 組測資。每組皆有兩個整數，代表年級 Y (分別為 1、2 或 3) 和體重 W。其中特別的是，年級非 1、2、3 者被視為非法玩家，不受魔咒影響

◆輸出說明：計算登出時體重

    #include <iostream>
    using namespace std;

    main()
    {
        int n, y, w;
        cin >> n;

        for ( int i = 0 ; i < n ; ++i )
        {
            cin >> y >> w;

            if ( y < 4 && y > 0 )
            {
                cout << w + 7*(4-y)<< endl;
            }
            else
            {
                cout << w << endl;
            }
        }

    }
    
## Unit 5 迴圈(while)

### 5-1.期間限定合作活動
HGSH online 決定和 HCHS online 舉辦期間限定合作活動，讓雙方玩家可以跨平台遊玩。

假設最初 HGSH 和 HCHS 有 A 和 B 個玩家投入活動

宣傳第一個禮拜，每過一天，前者增加 15 個、後者增加 5 個玩家

第二個禮拜開始，每過一天，前者增加 5 個、後者增加 15 個玩家


為了避免雙方遊玩比例失調，當有一方為對方兩倍(含)以上時，活動會提前終止，請問活動會在第幾天終止。

◆輸入說明：兩個正整數 A 和 B，分別代表 HGSH 和 HCHS 的初始玩家數

◆輸出說明：幾天後活動終止

    #include <iostream>
    using namespace std;

    int main()
    {
        int A, B, t =0;
        cin >> A >> B;

        while( !(A >= B*2 || B>= A*2) )
        {
            if(t < 7)
            {
                A = A + 15;
                B = B + 5;
            }
            else
            {
                A = A + 5;
                B = B + 15;
            }
            ++t;
        }

        cout << t << endl;

    }
    
### 5-2. 一人遊戲
因為巴斯的離開，胡迪覺得非常孤單，孤單到自己開始和自己玩起了遊戲。

這個遊戲是這樣的，他會先設定一個數字做為答案。

之後假裝不知道這個答案而開始猜數字，直到猜中為止。

如果猜的數字比答案小，顯示「oo 比答案小」

如果猜的數字比答案大，顯示「oo 比答案大」

如果猜的數字是正確答案，顯示「oo 就是正確答案」


◆輸入說明：第一行有一個整數，代表答案。之後有任意多行整數，代表嘗試猜的數字

◆輸出說明：猜數字的過程

對於每組嘗試猜的數字

如果猜的數字比答案小，顯示「oo 比答案小」

如果猜的數字比答案大，顯示「oo 比答案大」

如果猜的數字是正確答案，顯示「oo 就是正確答案」

    #include <iostream>
    using namespace std;

    int main()
    {
        int ans, guess;
        cin >> ans;
        while(true)
        {
            cin >> guess;

            if (guess == ans)
            {
                cout << guess << " 就是正確答案" << endl;
                break;
            }
            else if (guess < ans)
            {
                cout << guess << " 比答案小" << endl;
            }
            else
            {
                cout << guess << " 比答案大" << endl;
            }
        }
    }





