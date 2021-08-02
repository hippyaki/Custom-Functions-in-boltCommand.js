# GPIO Commands

## digitalWrite(pin,val)

pin: It is the Bolt GPIO you want to control. It can take any of the following values 0, 1, 2, 3, 4.
val: It is the output voltage to be provided on the GPIO. It can take value HIGH(3.3V) or LOW(0V).

Syntax - `digitalWrite(0,HIGH)`

Sample - 
```
 <button onclick="digitalWrite(0, HIGH);" > ON </button>
```

## digitalRead(pin,element_id)

pin: It is the Bolt GPIO you want to control. It can take any of the following values 0, 1, 2, 3, 4.
element_id: It is the ID parameter predefined in the function. We get a return in the ID in the form of innerHTML as **"Pin Val = 'value of pin' "**
value = HIGH/LOW

Syntax - `digitalRead(0,*myLight*)`

Sample -
```
<button onclick="digitalRead(0,'myLight');" > ON </button>
<br>
<div id = 'myLight'> </div>
```

## analogWrite(pin,val)

pin: It is the Bolt GPIO you want to control. It can take any of the following values 0, 1, 2, 3, 4.
val: It is the analog output voltage to be provided on the GPIO. It can take value between 0-255.

Syntax - `analoglWrite(0,150)`
```
 <button onclick="digitalWrite(0, 150);" > Check Pin Value </button>
```

## analogRead(pin,element_id)

pin: It is the Bolt GPIO you want to control. It can take value A0.
element_id: It is the ID parameter that returns in the form of innerHTML as **"Pin Val = 'value of pin' "**
value = range (0 - 1024)

Syntax - `analogRead(A0,*myLight*)`

Sample -
```
<button onclick="analogRead(A0,'myLight');" > Check Pin Value </button>
<br>
<div id = 'myLight'> </div>
```

## digitalMultiWrite(pins,val)

pins: It is the Bolt GPIO you want to control. It can take multiple no. of following values followed by comma (,)
val: It is the output voltage to be provided on the GPIO. It can take value HIGH(3.3V) or LOW(0V).

Syntax - `digitalMultiWrite('0,1,2','HIGH,LOW,HIGH')`

Sample - 
```
 <button onclick="digitalMultiWrite('0,1,2','HIGH,LOW,HIGH');" > ON </button>
```

## digitalMultiRead(pins,element_id)

pin: It is the Bolt GPIO you want to control. It can take multiple no. of following values followed by comma (,)
element_id: It is the ID parameter predefined in the function. We get a return in the ID in the form of innerHTML as **"Pin Val = 'value of pin' "**
value = HIGH/LOW

Syntax - `digitalMultiRead('0,1,2,3','*myLight*'')`

Sample -
```
<button onclick="digitalMultiRead('0,1,2,3','myLight');" > ON </button>
<br>
<div id = 'myLight'> </div>
```


## analogMultiWrite(pins,val)

pins: It is the Bolt GPIO you want to control. It can take multiple no. of following values followed by comma (,)
val: It is the analog output voltage to be provided on the GPIO. It can take value between 0-255.

Syntax - `analogMultiWrite('0,1,2','50,139,240')`

Sample - 
```
 <button onclick="analogMultiWrite('0,1,2','50,139,240');" > ON </button>
```

