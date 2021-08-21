# An introduction to game hacking

## Preface
So, you would like to become a game hacker;  But you are found asking yourself, "where do I begin?"  I hope I can provide an answer to your question, and to other questions that you may have.  In my series, I explain how to manipulate and reverse engineer game engines, as well as touch on specific game engines such as the Unity and Unreal Engine.  I provide basic examples of game cheats, such as Rust, to demonstrate the general structure of a game hack as well as guide you to making your own.  Furthermore, I also provide tutorials on using various different tools such as reclass, cheat engine, and ida to help in the revese engineering of the game.

## Prerequisites
To understand my series to its fullest extent, you should have a basic comprehension of assembly and c++ as well as a basic understanding of memory.

## The Basics
In this segment of the series, I will explain how to use tools such as reclass, cheat engine, and ida.

### Reclass
Reclass is a powerful tool used to view structs in memory as well as construct them.  Lets start with an example, the program I am using for this example can be found here: https://reclass.example

The code of the struct I am dissecting is as follows: 
```c++
struct dissect_me_t
{
	const std::uint64_t m1 = 0x1122334455667788, m2 = 0x8877665544332211;
};
```

I will first explain the common controls of reclass before we begin dissecting an example program.

To begin dissecting a program, click "file" -> "attach to process" -> find the process and click attach.

The interface of reclass is as follows:
![image](https://user-images.githubusercontent.com/75095310/130306174-ac9f98ec-a4e0-4c3a-bcf7-b21f20f2f786.png)

To create a new struct type, you would right click "classes" at the left hand side and click "add new class." 
<br />
![image](https://user-images.githubusercontent.com/75095310/130306219-730caa6c-1a64-4add-9c63-d483e77d0eb3.png)

To delete a class, simply right the class name under the "classes" tag, and select "Delete class"
<br />
![image](https://user-images.githubusercontent.com/75095310/130306312-32402a2b-570b-40e6-8b4d-7aacffde5d2f.png)

To view a struct in memory, click the address box, paste your address, and click enter
<br />
![image](https://user-images.githubusercontent.com/75095310/130306402-6356cf79-bd00-4145-ac4a-075dac29db85.png)
