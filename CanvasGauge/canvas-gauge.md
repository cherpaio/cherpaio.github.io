<div id="cg"></div>

# CanvasGauge
> Use a gauge to visualize a pin or a value.


<a target='_blank' rel='nofollow' href="https://s3-us-west-2.amazonaws.com/cherpa01-static/media/images/docs/gauge.png">  <img alt='Gauge' width="300px" src='https://s3-us-west-2.amazonaws.com/cherpa01-static/media/images/docs/gauge.png' class="center" /></a>


## Methods Available

- [myGauge.init()](CanvasGauge/canvas-gauge.md?id=cg-i-di)
- [myGauge.init(int min,int max, String title)](CanvasGauge/canvas-gauge.md?id=cg-i-iwp)
- [visualizePin(int pin)](CanvasGauge/canvas-gauge.md?id=cg-v-vp)
- [visualize(int value)](CanvasGauge/canvas-gauge.md?id=cg-v-vv)


<div id="cg-co"></div>

## Create object 
Create an object from **<code>CanvasGauge</code>** outside the **<code>setup()</code>** function

```       
CanvasGauge myGauge; 
	void setup(){ 
} 
	void loop(){  
}
```

<div id="cg-i"></div>

## Initialize

> Initialize **<code>CanvasGauge</code>** using one of two different methods


<div id="cg-i-di"></div>

* #### Default Initialization
Use **<code>myGauge.init()</code>** as follows:

	```
	void setup(){  
		myGauge.init(); 
	} 
	```


<div id="cg-i-iwp"></div>


* #### Initialization with parameters
Use **<code>myGauge.init(int min,int max, String title)</code>** as follows:
	```
	void setup(){  
		myGauge.init(0,100,”Pot value”); 
	} 
	```


<div id="cg-v"></div>


## Visualize


<div id="cg-v-vp"></div>


* #### Visualize Pin
Use the **<code>visualizePin(int pin)</code>** method as follows:
	
	```	
	void loop(){ 
		myGauge.visualizePin(A0); 	 
	}	 
	```

	<p class="tip">Note: The visualize method sets the visualized pin to an INPUT pin. </p>


<div id="cg-v-vv"></div>

* #### Visualize Value
Use the **<code>visualize(int value)</code>** method as follows:

	```
	void loop(){  
		myGauge.visualize(54); 
	} 
	```

<div id="ccg-cex"></div>

## Example Code
> Read the value of the Potentiometer connected to pin A0.

	CanvasGauge myGauge; 
	 
	void setup(){ 
	 
		myGauge.init(0,1023,”Pot value);  
	}
	 
	void loop(){ 
	 
		myGauge.visualizePin(A0); 
	} 

