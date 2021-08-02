# GPIO Commands

## digitalWrite(pin,val)

**pin:** It is the Bolt GPIO you want to control. It can take any of the following values 0, 1, 2, 3, 4.
**val:** It is the output voltage to be provided on the GPIO. It can take value HIGH(3.3V) or LOW(0V).

**Syntax** - `digitalWrite(0,HIGH)`

**Sample** - 
```
 <button onclick="digitalWrite(0, HIGH);" > ON </button>
```

## digitalRead(pin,element_id)

**pin**: It is the Bolt GPIO you want to control. It can take any of the following values 0, 1, 2, 3, 4.
**element_id**: It is the ID parameter predefined in the function. We get a return in the ID in the form of innerHTML as **"Pin Val = 'value of pin' "**
**value** = HIGH/LOW

**Syntax** - `digitalRead(0,'myLight')`

**Sample** -
```
<button onclick="digitalRead(0,'myLight');" > Check Pin Value</button>
<br>
<div id = 'myLight'> </div>
```

## analogWrite(pin,val)

**pin**: It is the Bolt GPIO you want to control. It can take any of the following values 0, 1, 2, 3, 4.
**val**: It is the analog output voltage to be provided on the GPIO. It can take value between 0-255 (PWM).

**Syntax** - `analoglWrite(0,150)`
```
 <button onclick="digitalWrite(0, 150);" > Pin Valye </button>
```

## analogRead(pin,element_id)

**pin**: It is the Bolt GPIO you want to control. It can take value A0.
**element_id**: It is the ID parameter that returns in the form of innerHTML as **"Pin Val = 'value of pin' "**
**value** = range (0 - 1024)

**Syntax** - `analogRead(A0,'myLight')`

**Sample** -
```
<button onclick="analogRead(A0,'myLight');" > Check Pin Value </button>
<br>
<div id = 'myLight'> </div>
```

## digitalMultiWrite(pins,val)

**pins**: It is the Bolt GPIO you want to control. It can take multiple no. of following values followed by comma (,)
**val**: It is the output voltage to be provided on the GPIO. It can take value HIGH(3.3V) or LOW(0V).

**Syntax** - `digitalMultiWrite('0,1,2','HIGH,LOW,HIGH')`

**Sample** - 
```
 <button onclick="digitalMultiWrite('0,1,2','HIGH,LOW,HIGH');" > ON </button>
```

## digitalMultiRead(pins,element_id)

**pin**: It is the Bolt GPIO you want to control. It can take multiple no. of following values followed by comma (,)
**element_id**: It is the ID parameter predefined in the function. We get a return in the ID in the form of innerHTML as **"Pin Val = 'value of pin' "**
**value** = HIGH/LOW

**Syntax** - `digitalMultiRead('0,1,2,3','myLight')`

**Sample** -
```
<button onclick="digitalMultiRead('0,1,2,3','myLight');" > Check PIN Values </button>
<br>
<div id = 'myLight'> </div>
```


## analogMultiWrite(pins,val)

pins: It is the Bolt GPIO you want to control. It can take multiple no. of following values followed by comma (,)
val: It is the analog output voltage to be provided on the GPIO. It can take value between 0-255 (PWM).
Syntax - `analogMultiWrite('0,1,2','50,139,240')`

Sample - 
```
 <button onclick="analogMultiWrite('0,1,2','50,139,240');" > ON </button>
```

<br>

# UART Commands

## serialBegin(baud)

**baud**: It is the baud rate at which information is transferred in a communication channel.  In the serial port context, "9600 baud" means that the serial port is capable of transferring a maximum of 9600 bits per second.

**IMPORTANT**: In the Cloud, baud is set to individual integers 0, 1, 2, 3 which signify 2400, 4800, 9600 and 19200 respectively. But when using function, make sure to write the rate instead of the baud set. Because boltCommand.js has the functions defined already to convert from baudrate to baudset.

**Syntax** - `serialBegin(9600)`

**Sample** - 
```
 <button onclick="serialBegin(9600);" > Start Serial Communication with 9600 baudrate </button>
```

## serialWrite(serialdata)

**serialdata**: dataString where String will be transmitted as ASCII characters

**Syntax** - `serialWrite(Hello)`

**Sample** - 
```
 <button onclick="serialWrite(Hello);" > Write 'Hello' on the Serial Monitor  </button>
```

## serialRead(till,element_id)

**till**: Read the data upto the specified 'till' value from the incoming UART data to Bolt. It takes ASCII value of the character from 0-127.
element_id: It is the ID parameter predefined in the function. We get a return in the ID in the form of innerHTML as **"Read Val = 'value present in serial monitor' "**
**
Syntax** - `serialRead('10','myLight')`

**Sample** -
```
<button onclick="serialRead('10','myLight');" > Read the Line till 'next line' is present  </button> // 10 is the ASCII character for '\n'
<br>
<div id = 'myLight'> </div>
```

## serialWR(data,till,element_id)

**data**: dataString where String will be transmitted as ASCII characters
till: Read the data upto the specified 'till' value from the incoming UART data to Bolt. It takes ASCII value of the character from 0-127.
**element_id**: It is the ID parameter predefined in the function. We get a return in the ID in the form of innerHTML as **"Read Val = 'value present in serial monitor' "**

**Syntax** - `serialWR('Hello','10','myLight')`

**Sample** -
```
<button onclick="serialWR('Hello','10','myLight');" > Write Hello and then Read the Line till 'next line' is present  </button>
<br>
<div id = 'myLight'> </div>
```

<br>

# Cloud Pro(only)

## servoWrite(pin,val)

**pin**: It is the Bolt GPIO you want to control. It can take any of the following values 0, 1, 2, 3, 4.
**val**: It is the degree of servo motor in terms of degree. It can take values between 0-180

**Syntax** - `servoWrite(0,HIGH)`

**Sample** - 
```
 <button onclick="servoWrite(0, 60);" > Turn Servo Motor 60 degree </button>
```

## servoRead(pin,element_id)

**pin**: It is the Bolt GPIO you want to control. It can take any of the following values 0, 1, 2, 3, 4.
**element_id**: It is the ID parameter predefined in the function. We get a return in the ID in the form of innerHTML as **"Pin Val = 'value of pin' "**
**value** = HIGH/LOW

**Syntax** - `servoRead(0,'myLight')`

**Sample** -
```
<button onclick="servoRead(0,'myLight');" > Check Servo Value </button>
<br>
<div id = 'myLight'> </div>
```
<br>

# Utilities

## setKey(key,dev_name)

**key**: This is your API key
**dev_name**: This is your DEVICE_ID

**Syntax** - `setKey('XXXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXX','BOLTXXXXXXX')`
