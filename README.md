# TextEffects
A wide variety of unique text effects for your C# console applications, all simplified in this library!

I feel like this is useless but yeah... I made a C# Library B)
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
Typewriter.Type();
Typewriter.TypeLine();
Typewriter.List();
Typewriter.TypeList();
```
### ```Type, TypeLine```
This is a simple effect that will allow you to easily integrate a typewritten animation.
```cs
Typewriter.Type(message, typeSpeed);
Typewriter.TypeLine(message, typeSpeed);
```

The 'message' must be defined using a ```String```.

The 'typeSpeed' parameter can only be defined using an ```Int``` type. As the name suggests, with this you can adjust the typing speed of the message.
### Example 001
### Code -
```cs
Typewriter.Type("Hello World!", 75);
```
### Output -
```
Hello World!
```
### Example 002
### Code -
```cs
Typewriter.TypeLine("Hello World!", 75);
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
### ```List, TypeList```
Similarly to ```Typeline```, this effect types out .
```cs
Typewriter.Typeline(effect, message, typeSpeed);
```

The 'message' must be defined using a ```String[]```.

The 'typeSpeed' parameter can only be defined using an ```Int``` type. As the name suggests, with this you can adjust the typing speed of the message.
### Example 003
### Code -
```cs
string[] myList =
{
    "1. Hello World!",
    "2. This is a list!",
    "3. It is typed by each letter and then line!",
    "Goodbye for now..."
};
Typewriter.Type(myList, 75);
```
### Output -
```
1. Hello World!
2. This is a list!
3. It is typed by each letter and then line!
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
Typewriter.TypeList(myList, 75);
```
### Output -
```
1. Hello World!
2. This is a list!
3. It is typed by each line!
Goodbye for now...
```

## Animation
### All instances -
```cs
Animation.Spinner();
```

### ```Spinner```
The spinner can be easily defined with just one short line and is suitable for when in the need 
```cs
Animation.Spinner(type, animSpeed, rotations);
```

The 'type' parameter must be defined using an ```Int```.

The 'animSpeed' parameter can only be defined using an ```Int``` type. As the name suggests, with this you can adjust the animation speed of the spinner.

The 'rotations' parameter, defined using an ```Int``` type, it sets the amount of rotations needed.

### Example 003
### Code -
```cs
Animation.Spinner(0, 100, 50);
```
### Output -
```
/-\\|
```
