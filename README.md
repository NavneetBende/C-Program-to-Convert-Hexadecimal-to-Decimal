# C-Program-to-Convert-Hexadecimal-to-Decimal

Hexadecimal to Decimal in C++
All of us would remember Mark Watney, a botanist, who with the help of Hexadecimal escaped mars. In this post, we will do a little to write. a Program Hexadecimal to Decimal in C.

But, first we must understand what Hexadecimals are. Hexadecimal are number system with base 15. Generally, all addresses in memory are indexed in Hexadecimal format

Hexadecimal Range - (0, 15)

With numbers (0 - 9) represented as is

And 10 - A, 11 - B, 12 - C, 13 - D, 14 - E, 15 - F 
Working of HexaDecimal to Decimal in C++
While loop in C
Different methods covered in the post
We will cover the following methods to do the conversion –

Algorithmic approach
Using inbuilt methods
Method 1
In this method, we use the algorithm to find conversion from hexadecimal to decimal. The knowledge of ASCII is important. Please check the ASCII table here –

Method 1 code in C++
Run
// C++ Program for Hexadecimal to Decimal Conversion
// C++ Program for Hexadecimal to Decimal Conversion
#include<iostream>

#include<math.h>


using namespace std;

int convert(string num)
{
    int len = num.size();
    int dec = 0, index = 0;
    
    for(int i = len - 1; i >= 0; i--)
    {
        // Here we check if current array char is between (0-9)
        if (num[i] >= '0' && num[i] <= '9') 
        {
            // whenever current num[i] is in range '0' - '9' 
            // ascii int value can be fetched 
            // by subtracting 48 (Refer Ascii table) as ASCII val 0 : 48 
            int digit = int(num[i]) - 48; 
            dec += digit * pow(16, index); 
            index++; 
        } 

        // Here we check if current array char is between (A-F) 
        else if (num[i] >= 'A' && num[i] <= 'F') 
        { 
            // whenever current num[i] is in range 'A' - 'F' 
            // ascii int value can be fetched 
            // by subtracting 55 (Refer Ascii table) as 
            // ASCII val A : 65 and A must result 10 as value 
            int digit = int(num[i]) - 55; 
            dec += digit * pow(16, index); 
            index++; 
        } 
    } 
    return dec; 
} 

int main() 
{ 
    string num; 
    cin >> num;
 
    cout << (convert(num));
 
    return 0;
}
Output
1F
31
Related Pages
Program for octal to decimal conversion

Program for hexadecimal to decimal conversion

Program for decimal to binary conversion

Program for decimal to octal conversion

Program for decimal to hexadecimal conversion

 

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
Method 2
The below method uses inbuilt functions to calculate the decimal equivalent of a hexadecimal number

Here we use the stoi(hexaDecimal_in_string_format, 0, base_value) method

Method 2 code in C++
Run
// Hexadecimal to decimal conversion using inbuilt methods in C++
#include<iostream>

using namespace std;
 
int main()
{
    string hexNumber;
    cin >> hexNumber;
    
    int base = 16;
    // format stoi(hexaDecimal_in_string_format, 0, base_value)
    cout << stoi(hexNumber, 0, base);
 
    return 0;
}
Output
3B7
951
