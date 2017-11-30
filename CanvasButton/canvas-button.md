<div id="cbb"></div>

# CanvasButton
> Control your circuit from a virtual button.

<a target='_blank' rel='nofollow' href="https://s3-us-west-2.amazonaws.com/cherpa01-static/media/images/docs/button.png">  <img alt='Button' src='https://s3-us-west-2.amazonaws.com/cherpa01-static/media/images/docs/button.png' class="center" /></a>

## Methods Available

- [myButton.init()](CanvasButton/canvas-button.md?id=cbb-i-di)
- [myButton.init(String title)](CanvasButton/canvas-button.md?id=cbb-i-iwp)
- [myButton.isOn()](CanvasButton/canvas-button.md?id=cbb-rv)
- [myButton.isff()](CanvasButton/canvas-button.md?id=cbb-rv)

<div id="cbb-co"></div>

## Create object 
Create an object from **<code>CanvasButton</code>** outside the **<code>setup()</code>** function

```       
CanvasButton myButton; 

void setup(){ 

} 

void loop(){ 

}
```

<div id="cbb-i"></div>

## Initialize

> Initialize **<code>CanvasButton</code>** using one of two different methods

<div id="cbb-i-di"></div>

* #### Default Initialization
Use <code>myButton.init()</code> as follows:

	```
	void setup(){  
		myButton.init();
	} 
	```


<div id="cbb-i-iwp"></div>


* #### Initialization with parameters
Use <code>myButton.init(String title)</code> as follows:
	```
	void setup(){  
		myButton.init(”LED Button”); 
	} 
	```


<div id="cbb-rv"></div>

## Reading value 
* #### Reading value from button
Use the **<code>myButton.isOn()</code>** or **<code>myButton.isOff()</code>**  method as follows:
	
	```	
	void loop(){ 

		if(myButton.isOn())
			digitalWrite(LED_PIN, HIGH);
		else if(myButton.isOff())
			digitalWrite(LED_PIN, LOW); 

	}	 
	```

<div id="cbb-cec"></div>


## Example Code

> Control buildt-in LED with a virtual button.

	CanvasButton myButton; 
	int const LED_PIN = 13; 

	void setup(){ 
		myButton.init(”LED Button”); 
		pinMode(LED_PIN,OUTPUT); 
	} 
	void loop(){

		if(myButton.isOn())
			digitalWrite(LED_PIN, HIGH); 
		else
			digitalWrite(LED_PIN, LOW);

		delay(500);
	} 


