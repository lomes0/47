### About

---



In a past job interview I have been asked the following question:

"Suggest functions which expect an input $x\in\{4,7\}$, and returns $\{4,7\} \setminus \{x\}$."

Meaning, come up with function s.t:

``` c++
/*
* @Desc: 
*	Receives 4 or 7.
* @Return:
*	4 if x=7.
*	7 if x=4.
*/
int foo(int x)
```



Here is what I got so far...

```c++
int foo(int x) {
	auto arr = {0,0,0,0,7,0,0,4};
	return arr[x];
}
```



```C++
int foo(int x) {
	return (x*10) % 33;
}
```



``` c++
int foo(int x) {
    if (x == 4) {
        return 7
    }
    return 4
}
```



```c++
int foo(int x) {
    switch x {
        case 4: return 7;
        case 7: return 4;
    }
    return 0;
}
```



``` c++
int foo(int x) {
    return x ^ 0x3;
}
```



~~~ C++
int foo(int x) {
    return |65/11 - x|(11/3);
}

int foo(int x) {
    return inverse(x / 28);
}

int foo(int x) {
    return (x - 10)(-1) + 1;
}

int foo(int x) {
    return (x-4)(4/3) + (7-x)(7/3);
}

int foo(int x) {
    # Where P is a rational function, s.t P(4)=7 and P(7)=4.
    return P(x);
}
~~~



```c++
int foo(int x) {

        int i = 0;
        std::thread t([&i, x]() {
                  
			/* sleep for x seconds */
	    	std::this_thread::sleep_for(std::chrono::seconds(x));
        	i = 3;
		});

        t.detach();

        /* sleep 6 seconds */
        std::this_thread::sleep_for(std::chrono::seconds(6));

        return 4 + i;
}
```

