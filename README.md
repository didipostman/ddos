# ddos
A tool conception for DDOs attack

Didipostman : my ddos white papaer conception

Author : Wadï Mami

Date : 05/03/2026

E-mail : wmami@steg.com.tn / didipostman77@gmail.com

In this paper I share with you what comes to my mind when seeing this Spring Batch Sequence diagram on 12/02/2012.

![01fig07](https://github.com/user-attachments/assets/4f813bde-8742-46c8-a058-8ba2379d265a)

Spring batch reads and reads till reaching commit-interval value and then writes all simultaneously.
So I said to myself Spring batch can read URLs (website addresses) and then attacks them in parallel in the itemWriter side by using simple code like https://github.com/naveen-98/DDOS-Java
And fitting this code to stand in the itemWriter Side by implmenting DdosAttackWriter which implements itemWriter.

Now (Spring Batch6) it is possible to run multiple Spring Batch instances in parallel before in Spring Batch 2 it is limited to only 20 it is just feasable by Only changing the parameters 
 What I mean is to use Spring Batch project without Spring Boot.
 So we can launch our SB_DdosAttack in parallel
java SB_DdosAttack -"11" 

java SB_DdosAttack -"12"

java SB_DdosAttack -"13"

…

.

.

.

java SB_DdosAttack -"1n"

This only for one JVM think we have multiple JVM multiple copy of jdk25 in our disk like the following

[PathToJDK1]/jdk1/bin/java SB_DdosAttack -"11"

[PathToJDK1]/jdk1/bin/java SB_DdosAttack -"12"

[PathToJDK1]/jdk1/bin/java SB_DdosAttack -"13"

.

.

.

[PathToJDK1]/jdk1/bin/java SB_DdosAttack -"1n"

[PathToJDK2]/jdk2/bin/java SB_DdosAttack -"21"

[PathToJDK2]/jdk2/bin/java SB_DdosAttack -"22"

[PathToJDK2]/jdk2/bin/java SB_DdosAttack -"23"

[PathToJDK2]/jdk2/bin/java SB_DdosAttack -"24"

....

[PathToJDK2]/jdk2/bin/java SB_DdosAttack -"2n"

...

..

.

.

.

[PathToJDKi]/jdki/bin/java SB_DdosAttack -"il"

.

..

[PathToJDKi]/jdki/bin/java SB_DdosAttack -"in"

Etc...


Conclusion : I just shared the conception fearing law persecutions but this tool can be used to test anti Ddos measurements. I think Didipostman is unbeatable 


