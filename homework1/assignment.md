''
#include <iostream>  
using namespace std;  
  
int main() {  
    int num1, num2;  
    int choice;  
    int result;  
  
    // 提示用户输入第一个整数  
    cout << "请输入第一个整数：";  
    cin >> num1;  
  
    // 提示用户输入第二个整数  
    cout << "请输入第二个整数：";  
    cin >> num2;  
  
    // 提示用户选择操作  
    cout << "请选择操作（1:加法，2:减法）：";  
    cin >> choice;  
  
    // 根据用户的选择执行相应的操作  
    switch(choice) {  
        case 1:  
            result = num1 + num2;  
            cout << "结果：" << num1 << " + " << num2 << " = " << result << endl;  
            break;  
        case 2:  
            result = num1 - num2;  
            cout << "结果：" << num1 << " - " << num2 << " = " << result << endl;  
            break;  
        default:  
            cout << "无效的选择，请输入1或2。" << endl;  
    }  
  
    return 0;  
}

![image](https://github.com/user-attachments/assets/a72bf2a8-7e8e-4a16-afc0-17a7c6c0e402)

''
#include <iostream>  
using namespace std;  
  
int main() {  
    int number;  
    cout << "请输入一个整数: ";  
    // 使用cin来接收用户输入的整数  
    cin >> number;  
  
    // 使用if-else语句来判断输入的数是奇数还是偶数  
    if (number % 2 == 0) {  
        // 如果余数为0，说明是偶数  
        cout << number << " 是偶数。" << endl;  
    } else {  
        // 如果余数不为0，说明是奇数  
        cout << number << " 是奇数。" << endl;  
    }  
  
    return 0;  
}

![image](https://github.com/user-attachments/assets/de119f92-13c6-48b2-9515-61e1e2ae9b27)

''
#include <iostream>  
#include <cstdlib> // 包含rand()和srand()  
#include <ctime>   // 包含time()  
  
using namespace std;  
  
int main() {  
    // 初始化随机数生成器  
    srand(time(0));  
  
    // 生成1到10之间的随机数  
    int secretNumber = rand() % 10 + 1;  
  
    // 声明变量来存储用户的猜测和猜测次数  
    int guess;  
    int guessCount = 0;  
  
    // 提示用户开始游戏  
    cout << "我想了一个 1 到 10 之间的数字，请猜一猜：" << endl;  
  
    // 使用while循环让用户多次猜测，直到猜对为止  
    while (true) {  
        cout << "你的猜测: ";  
        cin >> guess; // 读取用户输入  
  
        guessCount++; // 猜测次数加1  
  
        // 判断用户的猜测是否正确  
        if (guess == secretNumber) {  
            cout << "恭喜你，猜对了!你总共猜了 " 
