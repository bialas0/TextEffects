# TextEffects
A wide variety of unique text effects for your C# console applications, all simplified in this library!
# Installation Instructions
### Visual Studio Code
#### 1. Download and extract zip file.
#### 2. Place the .DLL file in your project file, preferably in a DLL folder.
#### 3. Reference the .DLL in the .CSPROJ file
```cs
    <ItemGroup>
     <Reference Include="TextEffects">
       <HintPath>..\Dlls\TextEffects.dll</HintPath>
     </Reference>
    </ItemGroup>
```
### Visual Studio 2022
#### 1. Download and extract zip file.
#### 2. Place the .DLL file in your project file, preferably in a DLL folder.
#### 3. Reference the .DLL in the Reference Manager.
![image](https://user-images.githubusercontent.com/118835576/210154186-ca1d5998-d3c1-4119-bb55-1a08169e04f6.png)

# Documentation
## Target Language: C#
## Target Framework: .NET 6.0 (LTS)
## Usage
Make sure to include the library before proceeding any further.
```cs
using TextEffects;
```
## Typewriter
### All instances -
```cs
Typewriter.Typeline();
Typewriter.TypeList();
```
### ```Typeline```
This is a simple effect that will allow you to easily integrate a typewritten animation.
```cs
Typewriter.Typeline(effect, message, typeSpeed);
```
The 'effect' can be defined using a ```Char```, either ```x``` or ```y```.

```x``` - This will typewrite the contents of the message horizontally.

```y``` - This will typewrite the contents of the message vertically.

The 'message' must be defined using a ```String```.

The 'typeSpeed' parameter can only be defined using an ```Int``` type. As the name suggests, with this you can adjust the typing speed of the message.
### Example 001
### Code -
```cs
Typewriter.Typeline('x', "Hello World!", 75);
```
### Output -
```
Hello World!
```
### Example 002
### Code -
```cs
Typewriter.Typeline('y', "Hello World!", 75);
```
### Output -
```
H
e
l
l
o

W
o
r
l
d
!
```
### ```Typelist```
Similarly to ```Typeline```, this effect types out .
```cs
Typewriter.Typeline(effect, message, typeSpeed);
```
The 'effect' can be defined using a ```Char```, either ```w``` or ```l```.

```w``` - This will typewrite the contents of the message line-by-line.

```l``` - This will typewrite the contents of the message letter-by-letter for each line.

The 'message' must be defined using a ```String[]```.

The 'typeSpeed' parameter can only be defined using an ```Int``` type. As the name suggests, with this you can adjust the typing speed of the message.
### Example 003
### Code -
```cs
string[] myList =
{
    "1. Hello World!",
    "2. This is a list!",
    "3. It is typed by each line!",
    "Goodbye for now..."
};
Typewriter.Typelist('w', myList, 75);
```
### Output -
```
1. Hello World!
2. This is a list!
3. It is typed by each line!
Goodbye for now...
```
### Example 004
### Code -
```cs
string[] myList =
{
    "1. Hello World!",
    "2. This is a list!",
    "3. It is typed by each line!",
    "Goodbye for now..."
};
Typewriter.Typelist('l', myList, 75);
```
### Output -
```
1. Hello World!
2. This is a list!
3. It is typed by each letter and then line!
Goodbye for now...
```
