# 高二資訊科技課堂作業

## Unit 1 程式語言介紹
### Hello World
"Hello world!"一支最基礎的程式，一句來自電腦世界的問候，同時也是許多人接觸到的第一個範例程式。

請輸出 Hello world!

    #include <iostream>
    using namespace std ;

    int main()
    {
        cout << "Hello world!" << endl ;
    }

## Unit 2 變數運算與輸入輸出

### BMI 計算機
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

