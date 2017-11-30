<div id="cs"></div>

# CanvasSlider
> Control your circuit from a virtual slider.

<a target='_blank' rel='nofollow' href="https://s3-us-west-2.amazonaws.com/cherpa01-static/media/images/docs/slider.png">  <img alt='Slider' src='https://s3-us-west-2.amazonaws.com/cherpa01-static/media/images/docs/slider.png' class="center" /></a>

## Methods Available

- [mySlider.init()](CanvasSlider/canvas-slider.md?id=cs-i-di)
- [mySlider.init(int min,int max, String title)](CanvasSlider/canvas-slider.md?id=cs-i-iwp)
- [mySlider.getValue()](CanvasSlider/canvas-slider.md?id=cs-rv)

<div id="cs-co"></div>

## Create object 
Create an object from **<code>CanvasSlider</code>** outside the **<code>setup()</code>** function

```       
CanvasSlider mySlider; 

void setup(){ 

} 

void loop(){ 

}
```

<div id="cs-i"></div>

## Initialize

> Initialize **<code>CanvasSlider</code>** using one of two different methods

<div id="cs-i-di"></div>

* #### Default Initialization
Use <code>mySlider.init();</code> as follows:

	```
	void setup(){  
		mySlider.init();
	} 
	```


<div id="cs-i-iwp"></div>


* #### Initialization with parameters
Use <code>mySlider.init(int min,int max, String title)</code> as follows:
	```
	void setup(){  
		mySlider.init(0,100,"Temperature meter"); 
	} 
	```


<div id="cs-rv"></div>

## Reading value 
* #### Reading value from slider
Use the <code>mySlider.getValue();</code> method as follows:
	
	```	
	void loop(){ 
		mySlider.getValue(); 
	}	 
	```

<div id="cs-cec"></div>


## Example Code

> Control LED brightness from virtual slider connected to pin 9.

	CanvasSlider mySlider; 
	int const LED_PIN = 9; 
	void setup(){ 
		mySlider.init(0,1023,"LED Brightness"); 
		pinMode(LED_PIN,OUTPUT); 
	} 
	void loop(){ 
		int sliderValue = mySlider.getValue(); 
		analogWrite(LED_PIN, sliderValue);

		delay(500);
	} 


