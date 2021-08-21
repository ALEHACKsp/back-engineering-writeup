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
To begin dissecting the program, follow the instructions below:

![](https://i.imgur.com/iXUxfXL.png)
![](https://i.imgur.com/YIS7RPW.png)
<br/>
<br/>
![](https://i.imgur.com/tmaE2wR.png)
