Simona Trajko 213237

**Control Flow Graph**

<img width="490" alt="image" src="https://github.com/simonatrajko/SI_2023_lab2_213237/assets/126770010/6ff36c5f-fbb4-4d36-a2d0-fab74912701b">

**Цикломатска комплексност**

Цикломатската комплекстност на овој јазол е 12, истата ја добив со формулата R каде што R е бројот на региони во Control Flow Graph-от.

**Every Branch kriterium**

<img width="1008" alt="image" src="https://github.com/simonatrajko/SI_2023_lab2_213237/assets/126770010/3fd5fc54-f30e-44cd-ba6c-2ee4039c7a62">

**Multiple Condition критериумот**

				if (user==null || user.getPassword()==null || user.getEmail()==null)
	T	T	T	T
	T	T	F	T
	T	F	T	T
	T	F	F	T
	F	T	T	T
	F	T	F	T
	F	F	T	T
	F	F	F	F
				
Можни случаи за следноит пример се:				
	T	*	*	T
	F	T	*	T
	F	F	T	T
	F	F	F	F
  
 - за првиот случај каде што доволно е само user==null да е точно односно треба usetr==null другите два услови се не битни
 - за вториот случај каде што user!=null додека user.getPassword()==null другиот услов не ебитно дали ќе биде точен или не
 - за третиот случај првиот и вториот улов треба да се неточно односно user!=null  и user.getPassword()!=null додека user.getEmail()==null 
 - за четвртиот случај треба сите три услови да бидат неточни и само во овој случај целиот израз е не точен односно тест примерот би изгледал user!=null  и user.getPassword()!=null и user.getEmail()!=null 
 
