# MAE540-Homework-1---Team-number-four
Testing of Softpot Membrane Potentiometer

## Introduction to the SoftPot Membrane Potentiometer

1. The SoftPot membrane potentiometer acts as an infinitely variable analog voltage divider. 
2. SoftPot Membrane Potentiometer is a very thin variable potentiometer.
3. We can vary the resistance linearly from 10 ohms to 10,000 ohms by pressing down on the various parts of the strip, allowing the user accurately calculate the relative position on the strip.
4. It consists of three layers: **Top layer with silver shunt, Space layer and Bottom layer with conductive carbon**.
5. Top layer closes the bottom layer when actuated, thus producing a reading. 
6. It be used as an accurate positional indicator for CNC head positioning, variable user input, straight user input and many other applications.

### Features of SoftPot

1. Lower cost than Mechanical Potentiometers
2. Sealed for harsh environments
3. Polyester substrate
4. Low set-up costs with versatility of custom design. 
5. Small [form factor][1].
6. We can combine multiple SoftPot on the same control panel.

### Specifications of SoftPot

1. Mounting Type : Custom
2. Operating Temperature Range : -40°C to 50°C
3. Resistance tolerance: ± 20%
4. Resistance (ohms) : 10K



[1]: https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=form+factor

## Adruino Code and Blynk Setup

Below is the code we put in adruino to get pin 5 to "HIGH".

{% highlight C linenos %}
	  #include <Wire.h>
	  #include <ESP8266WiFi.h>
	  #include <BlynkSimpleEsp8266.h>
	  
	  // You should get Auth Token in the Blynk App.
	  // Go to the Project Settings (nut icon).
	  char auth[] = "87fd9561fc854da99451724d1bde9d40"; 
	  
	  // Your WiFi credentials.
	  // Set password to "" for open networks.
	  char ssid[] = "Fawzan's iPhone"; 
	  char pass[] = "12345678"; 
	  
	  void setup()
	  {
	    Blynk.begin(auth, ssid, pass);
	  }
	  
	  void loop()

	  {
	    Blynk.run();
	  }
{% endhighlight %}

  
In Blynk, we created a new widget called "Gauge" and gave input as analog ADC0, this is shown in the pictures below.

<img src="https://i.imgsafe.org/6f2acd8992.png" alt="Drawing" style="height: 400px;"/>
<img src="https://i.imgsafe.org/6f2ad54359.png" alt="Drawing" style="height: 400px;"/>
