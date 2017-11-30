<div id="cb"></div>

# CanvasBarmeter
> Use a barmeter to visualize a pin or a value.

<a target='_blank' rel='nofollow' href="https://s3-us-west-2.amazonaws.com/cherpa01-static/media/images/docs/barmeter.png">  <img alt='Barmeter' src='https://s3-us-west-2.amazonaws.com/cherpa01-static/media/images/docs/barmeter.png' class="center" /></a>


## Methods Available

- [myBarmeter.init()](CanvasBarmeter/canvas-barmeter.md?id=cb-i-di)
- [myBarmeter.init(int min,int max, String title)](CanvasBarmeter/canvas-barmeter.md?id=cb-i-iwp)
- [visualizePin(int pin)](CanvasBarmeter/canvas-barmeter.md?id=cb-v-vp)
- [visualize(int value)](CanvasBarmeter/canvas-barmeter.md?id=cb-v-vv)


<div id="cb-co"></div>

## Create object 
Create an object from **<code>CanvasBarmeter</code>** outside the **<code>setup()</code>** function

```       
CanvasBarmeter myBarmeter; 
	void setup(){ 
} 
	void loop(){  
}
```

<div id="cb-i"></div>

## Initialize
> Example final code


<div id="cb-i-di"></div>

* #### Default Initialization
Use **<code>myBarmeter.init()</code>** as follows:

	```
	void setup(){  
		myBarmeter.init(); 
	} 
	```


<div id="cb-i-iwp"></div>


* #### Initialization with parameters
Use **<code>myBarmeter.init(int min,int max, String title)</code>** as follows:
	```
	void setup(){  
		myBarmeter.init(0,100,” Temperature meter”); 
	} 
	```


<div id="cb-v"></div>


## Visualize


<div id="cb-v-vp"></div>


* #### Visualize Pin
Use the **<code>visualizePin(int pin)</code>** method as follows:
	
	```	
	void loop(){ 
		myBarmeter.visualizePin(A0); 	 
	}	 
	```

	<p class="tip">Note: The visualize method sets the visualized pin to an INPUT pin. </p>


<div id="cb-v-vv"></div>

* #### Visualize Value
Use the **<code>visualize(int value)</code>** method as follows:

	```
	void loop(){  
		myBarmeter.visualize(54); 
	} 
	```

<div id="ccb-cex"></div>

## Example Code
> Read the value of the Temperature sensor connected to pin A0.

	CanvasBarmeter myBarmeter; 
	 
	void setup(){ 
	 
		myBarmeter.init(0,1023,"Temperature meter");  
	} 
	 
	void loop(){ 
	 
		myBarmeter.visualizePin(A0); 

		delay(500);
	} 

