# 54148
54f37y &amp; 53cur17y 1n 50f7w4r3 &amp; 5y573m5 148


Prove that you are a hacker (i.e. problem solver)

Being a hacker means you do not leave a problem unsolved because it is written in Haskell.
Before joining S4Lab, you need to prove that you are a hacker, to do so, please answer the following questions:

----

### 1-Many websites expose their “.git” files, please show how it could be dangerous.

websites expose their “.git” => Source Code Exposure vulnerability
“.git” keep track of all modifications on files or folders in projects. When .git folder is also deployed along with the web application, the attacker could exploit this misconfiguration to download the entire files(Even if it has already been deleted!)
#### Possible Impacts of .git Source Code Exposure Vulnerability:
* Access to Application Source Code :)
* Sensitive Data(Hardcoded Password, Database Credentials, API keys, etc.)
* Custom Algorithms
* Libraries
* Attacker can discover more vulnerabilities which may escalate to more dangerous attacks, which may be unknown to the attacker since the source code wasn’t accessible. 

#### Examples
* Just search  "intext: "index of /.git"" in google to find examples

#### Tools for extract all the available data:
* [GitTools](https://github.com/internetwache/GitTools)
* [GitHacker](https://github.com/WangYihang/GitHacker)
----

### 2-Imagine that we have 2**48 text files. Explain how can we find which files are the same.

Just do the following steps :
* Sort files by size 
* Calculate and compare the Hash of files that are the same size (use SHA256)
* For more certainty, we can compare similar files line by line

----
### 3- Write a hello-world C program and explain how we can dump its binary code with radare2.

#### Simple C program to display "Hello World"

```
#include <stdio.h>
int main()
{
    // prints hello world
    printf("Hello World");
    return 0;
}
```
#### Compile the code

 ```
 gcc -o helloworld HelloWorld.c
 ```
 
#### Dump helloworld binary code

```
r2 -q -c 'pi $s' ./helloworld > helloworld.txt
```
