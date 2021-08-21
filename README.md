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

To expand the view of a struct in memory, right click anywhere in the struct view, and click "Add Bytes."  You can then select the amount of bytes you wish to add to the view.
<br />
![image](https://user-images.githubusercontent.com/75095310/130306677-98249a10-b8a9-45c9-93af-d73657bf6126.png)

To change a node's type, right click on the node, and select "Change Type."  You can then select the type you wish to apply.
<br />
![image](https://user-images.githubusercontent.com/75095310/130306754-a8d910dc-8e4a-4807-8297-dfec630526d7.png)

To convert a node to a class within reclass, right click the node, and select "Create Class from Node(s)."  This is used to convert a struct within memory to a customizable struct within reclass.  The second image is an example of a struct within the current one.  On the left hand side, you can see the corresponding struct to the one inside the struct memory view.
<br />
![image](https://user-images.githubusercontent.com/75095310/130306789-f1d52687-c9a2-431b-b73b-4d50f0ca895f.png)
![image](https://user-images.githubusercontent.com/75095310/130306844-0adc805f-623c-4147-b1fd-6aba9097aa5d.png)

These are the most used controls within reclass;  Now we can begin dissecting our example program.

If you have not done already, please start "reclass-example.exe" and attach to it, as explained above.
