<div id="cb"></div>

# CanvasBarmeter
> Lorem ipsum dora explora Lorem ipsum dora explora Lorem ipsum dora explora Lorem ipsum dora explora

## Methods Available

- [myBarmeter.init()](CanvasBarmeter/canvas-barmeter.md?id=cb-i-di)
- [myBarmeter.init(int min,int max, String title)](CanvasBarmeter/canvas-barmeter.md?id=cb-i-iwp)
- [visualizePin(int pin)](CanvasBarmeter/canvas-barmeter.md?id=cb-v-vp)
- [visualize(int value)](CanvasBarmeter/canvas-barmeter.md?id=cb-v-vv)


<div id="cb-co"></div>

## Create object 
Lorem ipsum **<code>dora explora</code>** Lorem ipsum **<code>dora explora</code>**

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
> Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum Lorem ipsum 

	CanvasBarmeter myBarmeter; 
	 
	void setup(){ 
	 
		myBarmeter.init(0,1023,” Temperature meter”);  
	} 
	 
	void loop(){ 
	 
		myBarmeter.visualizePin(A0); 
	} 

