```ngMeta
name: Function Arguments
```

## What are function arguments?

Abhi tak humne jo bhi functions code kare hain, unme kuch bahot simple print statements hain. Hum aise functions bhi likh sakte hain jo kuch data leke uss data ke saath kuch karte hain. Iss code ko chala ke dekho.

```python
numbers_list = [1, 2, 3, 4, 5, 6, 7, 10, -2]
print (max(numbers_list))
```

**Output :-**
`10`

Yahan humne `max` function ko `numbers_list` di aur usne usme se sabse badi value hume de di. 

**max** function, python ka ek pre-defined function hai jise hum use kar sakte hai aur iske liye hume def max( ) likh kar usme code likhne ki koi jarurat nahi hai kyuki python banane wale ne humare liye ye kaam pehle hi kar diya hai.

Aise hi len function bhi ek list leke hume list mein items ki ginti deta hai.

len( ) function ka use hum kisi array ya sequence ki length find karne ke liye karte hai.Yeh  bhi python mai pre-define function hai.

`Example :-`

```python

a=[1,2,3,4,5,6]
print(len(a))
 ```

**Output :-**
6

Neeche diye gaye code ko chala ke dekho aur ek baar socho ki kya ho raha hai.

```python
def say_hello(name):
    print("Hello ", name)
    print("Aap kaise ho?")
say_hello("Aatif")
 ```
**Output :-**

Hello , Aatif
Aap kaise ho?


Yahan humne function ko ussi tareeke se define kiya hai jaise pichle examples mein kiya tha. Lekin dhyan se dekho toh `def say_hello` ke baad brackets mein humne `name` likha hai aur, aur neeche ek `name` variable ko print command ke saath use kar rahe hain. Yahan name ko *parameter* kehte hain jiski value hum function call karne ke time de sakte hain. Aakhri line mein function call karte vakt humne brackets ke andar `"Aatif"` likha hai. Function call karte vakt hum jo parameters ko value dete hain, unko arguments kehte hain.

Toh basically humne iss example mein yeh kiya aur seekha:

* `say_hello` naam ka ek function define kiya jo ek `name` naam ka parameter leta hai aur uska use kar ke kuch print karta hai
* fir humne function call kiya aur function call karne ke time ek argument diya jiski value "Aatif" thi
* jab yeh function call hota hai toh jo humne string "Aatif" argument diya hai. Yahan uski value name parameter mein jaati hai aur. Jab yeh value
* `name` parameter mein jaati hai, toh woh function ke andar same naam ke variable mein use kar sakte hain. Humne iss variable ka naam use kar ke print command likhi hai.

**Note: Yeh thoda sa mushkil concept, agar bahot ache se samajh nahi aaya, toh ek aur baar padh ke aur dusre examples dekh ke zaroor samajh aa jayega ;-)**

## Multiple Function Arguments

Abhi tak humne ek function argument ke saath hi code likha hai. Ab hum thode aur function arguments ke saath code likhte hain.

```python
def add_numbers(number1, number2):
    print("Main do numbers ko add karunga.")
    print(number1 + number2)
add_numbers(120, 50)
num_x = 134
name = "Rinki"
add_numbers(num_x, name)
 ```

**Output :-**

Main do numbers ko add karunga.
170
Main do numbers ko add karunga.

TypeError: unsupported operand type(s) for +: 'int' and 'str'



Yahan humne ek `add_numbers` naam ka function define kara hai. Lekin dekho ki bracket mein humne 2 parameter likhe hain. Ek sa jyada argument lene ke liye arguments ke baad comma laga dete hain Humne add_numbers(120, 50) likh ke function call karte samay do integer parameter diye hai. Yahan parameters ka kram / order important hai. Iss function call mein yeh hota 

* `120` ki value *pehle parameter* `number1` mein jaati hai jo ki function ke andar same naam ke variable number1 mein hai
* `50` ki value *dusre parameter* `number2` mein jaati hai jo ki function ke andar same naam ke variable number2 mein hai
* Baad mein humne do variable define kare hain, `num_x` and `num_y` aur fir add_numbers ko num_x aur num_y arguments deke call kiya hai. Yahan bhi:
* `num_x` ki value `134` pehle parameter `number1` mein jaati hai aur `num_y` ki value `Rinki` dusre parameter `number2` mein jaati hai.

Aur ache se samajhne ke liye ek aur example dekhte hain.


Jese ki apne dekha ki **output** mai **TypeError** aa rahi kuki hum kabhi bhi string aur integer concate nahi kar sakte hai.Humne num_1 mai **integer** store kiya aur name mai **string** store kiya hai.


```python
def say_hello_language(name, language):
    if language == "hindi":
        print("Namaste ", name)
        print("Aap kaise ho?")
    elif language == "punjabi":
        print("Sat sri akaal ", name)
        print("Tuhada ki haal hai?")
    else:
        print("Hello ", name)
        print("How are you?")
say_hello_language("Rishabh", "punjabi")
say_hello_language("Armaan", "english")
say_hello_language("Abhishek", "french")
say_hello_language("Kavay", "hindi")
 ```
**Output :-**


Sat sri akaal  Rishabh
Tuhada ki haal hai?
Hello  Armaan
How are you?
Hello  Abhishek
How are you?
Namaste  Kavay
Aap kaise ho?

Yeh function do parameter leta hai, `name` aur `language` aur aise kaam karta hai:

* Agar `language` `"hindi"` di hai, toh hindi mein kuch print karega
* Agar `language` `"punjabi"` di hai, toh punjabi mein kuch print karega
* Agar `"hindi"` aur `"punjabi"` ke ilava koi bhi language di hai toh english mein karega

Yeh karne ke liye humne ek function define kiya jo do arguments leta hai, `name` aur `language`. Hum jab `say_hello_language("Rishabh", "punjabi")` call karte hain toh yeh hota hai:

* Pehle parameter, `name` mein "Rishabh" string jata hai aur dusre parameter, `language` mein punjabi jaata hai.
* Fir humara program if-elif-else ka use kar ke dekhta hai language ki value kya hai aur uske hisaab se sahi language mein print kar deta ha
* Isi tareeke se upar likhi hui saari function calls mein yeh hi hota hai


## Ek aur example

Chalane se pehle isko padh ke output ko sochne ki koshish karo. Fir chala ke dekho ki aapne sahi output sochi thi ya nahi.

```python
def say_hello_people(name_x, name_y, name_z, name_a):
    print("Namaste ", name_x) # hindi mein
    print("Alah hafiz ", name_y) # urdu mein
    print("Bonjour ", name_z) # french mein
    print("Hello ", name_a) # english mein
say_hello_people("Imitiyaz", "Rishabh", "Rahul", "Vidya")
say_hello_people("Steve", "Saswata", "Shakrundin", "Rajeev")
 ```
**Output :-**


Namaste  Imitiyaz
Alah hafiz  Rishabh
Bonjour  Rahul
Hello  Vidya
Namaste  Steve
Alah hafiz  Saswata
Bonjour  Shakrundin
Hello  Rajeev


Iss function mein dekho ki yeh 4 argument leta hai, `name_x`, `name_y`, `name_z`, `name_a`. `def` waali pehli line mein humne 4 parameter ka naam comma (`,`) laga laga ke likhe hain. Function call karte samay jis kram / order mein humne parameters likhe hain def waali line mein, wahi kram / order mein arguments ki value parameters mein jaati hai.

`say_hello_people("Imitiyaz", "Rishabh", "Rahul", "Vidya")` mein parameters ki value iss hisaab se jaati hain:

* `"Imtiyaz"` ki value pehle parameter `name_x` mein jaati hai
* `"Rishabh"` ki value dusre parameter `name_y` mein jaati hai
* `"Rahul"` ki value teesre parameter `name_z` mein jaati hai
* `"Vidya"` ki value teesre parameter `name_a` mein jaati hai

## Python Arbitrary Arguments 

Arbitrary arguments hum tab use karte hai jab hume pata nahi hota hai ki hume kitne no. of arguments function mai dene hai. Hum arbitrary arguments ke sath function of define karne ke liye parameter se pehle ( * ) ka use karte hai jai ki neeche dikhaya gaya hai.

`Example:-`

```python
def icecream(*flavours):
 for flavour in flavours:
  print("i love"+flavour)

icecream("chocolate", "butterscotch","vanilla","strawberry")
 ```

**Output :-**


i love chocolate
i love butterscotch
i love vanilla
i love strawberry 


## Default parameter value  

Default parameter value se yaha humara ye matlab hai ki hum function ko define karte time kisi parameter ko value assign kar dete hai taaki hum function ko bina kisi argument ke call kare to vo default value ko le le.

`Example :-`

```python
def attendance(name,status="absent"):
	print(name,"is",status," today")

attendance("kartik","present")
attendance("sonu")
attendance("vishal","present")
attendance("umesh")
 ```

**Output :-**

kartik is present today
sonu is absent today
vishal is present today
Umesh is absent today
