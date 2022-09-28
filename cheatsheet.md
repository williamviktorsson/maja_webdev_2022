# Cheat sheet

## `Typer`
```js
// let variabelnamn = värde (värdet har en typ t.ex. number/string/list/object)
// Vi säger att vi tilldelar ett värde av en viss typ till en variabel med ett namn
// Variabelnamn har bokstäver i sig och kan ha siffror i sig. 
// Endast vissa specialtecken är tillåtna i variabelnamnen.
let x_str = "hello" 
let x_float = 20.5
let x_int = 5
let x_list = [1,2,3,4] 
let x_object = {name:"bart",age:13}
let x_var = x_int // x_var får värdet som x_int har när datorn exekverar tilldelningen,
let x_true = true
let x_false = false
```

## `Aritmetiska operationer`
```js
//     +          -              *           /         %          **
// addition, subtraktion, multiplikation, division, modulus, exponentiering

let add_result      = 5 + 5.5     // 10.5
let subtract_result = 12.5 - 15   // -2.5
let division_result = "15"/3 // 5
let modulus_result  = 7 % 3       // 1
let exponent_result = 2**4        // 16

let fancy_string = "hello agent nr." + exponent_result + (" how are u?" * 5)
let fancier_string = `hello lucky number ${division_result}`

let example = 5 + null    // returns 5         because null is converted to 0
    example = "5" + null  // returns "5null"   because null is converted to "null"
    example = "5" + 2     // returns "52"      because 2 is converted to "2"
    example = "5" - 2     // returns 3         because "5" is converted to 5
    example = "5" * "2"   // returns 10        because "5" and "2" are converted to 5 and 2


```

## `Kontrollstrukturer`
```js
// Vi använder if/elif/else för att styra vilken bit kod som körs.
// Varje if eller elif följs av ett villkor.
// Ett villkor är ett uttryck som datorn utvärderar till true eller false

// Dessa uttryck kallas booleanska uttryck

if (5 > 6){
    console.log("5 is larger than 6")
}
else if (6 > 6) {
    console.log("6 is larger than 6")
}
else {
    console.log("6 is larger than some number")
}
```

<div style="page-break-after: always;"></div>


## `Villkor`
```js
if (6==6){
    console.log("6 equals 6")
}
if (4!=6){
    console.log("4 is not equal to 6")
}
if (4<6){
    console.log("4 is less than 6")
}
if (4<=4){
    console.log("4 is less than or equal to 4")
}
if (10>5){
    console.log("10 is more than 5")
}
if (10>=10){
    console.log("10 is more than or equal to 10")
}
if !(5==6){
    console.log("5 is not equal to 6")
}
if ((2==2) && (5==5)){
    console.log("2 equals 2 and 5 equals 5")
}

if ((3==3) || (not 1==1)){
    console.log("3 equals 3 or 1 does not equal 1")
}
```

## `Listor`
```js
x_list = [1,2,3,4,5]    // skapa en ny lista
x_list.pop()            // ta bort längst bak
x_list.shift()           // ta bort längst fram
x_list.push(10)       // lägg till 10 längst bak
x_list.unshift(5)       // lägg till 5 längst fram

console.log(x_list)           // skriv ut listan: [5,2,3,4,10]
```

## `for-loopar`
```js
// använd en for-loop för att exekvera något för varje element i en lista
let x_list = [1,2,3,4,5]
for (let i = 0; i<x_list.length;i++){
    let element = x_list[i]
    console.log(element)
}

// använd en for-loop för att göra något 100 gånger
for (let i = 0; i<100;i++){
    console.log(i)
}
```

## `while-loopar`
```js
// använd en while-loop för att göra något så länge ett booleanskt uttryck är sant
let num = 0
while (num < 10){
    console.log(num)
    num = num+1
}


// eller så länge en listas längd inte är ett visst värde
let x_list = []
while (x_list.length!=10){
    x_list.push(1)
}
console.log(x_list)

// eller om du vill göra olika saker på jämna och udda varv
let x_num = 0
while (x_num<1000){
    if(x_num%2==0){
        console.log(x_num+" is even")
    }
    else{
        console.log(x_num+" is odd")
    }
    x_num = x_num+1
}

```

## `object/map/dictionary`
```js
x_object = {name:"bart",age:13}
console.log(x_object["name"]) // skriv ut värdet kopplat till nyckeln "name"
console.log(x_object.age)
delete x_object.name
console.log(x_object)
```

<div style="page-break-after: always;"></div>

## `funktioner`
```js
// funktionen tar inga "argument"
// funktionen returnerar inga värden
function example(){
    console.log("pancakes")
}

// anropa funktionen
example()
example()
example()

// funktionen tar inga "argument"
// funktionen returnerar ett värde
function example(){
    return "Chocolate"
}

// anropa funktionen
let temp = example()
temp = temp + example()
temp = temp + "Rainbow"
console.log(temp)

// funktionen tar två "argument". De värden vi skickar in till funktionen kommer
// funktionen åt genom att använda argumenten "first" eller "second"
// ni kan kalla dessa argument vad ni vill
// om det finns variabler i programmet med samma namn som argumenten spelar ej roll
// funktionen returnerar inget värde
function addition(first,second){
    console.log(first+second)
}

 // "ABC" tilldelas till first, "123" till first
addition("ABC","123")
 // 20 tilldelas till first, 40 till first
addition(20,20)
let cash = 400
let reward = 200
 // variabeln cash tilldelas till first, variabeln reward till second
addition(cash,reward)

// funktionen returnerar ett värde
// vi kan t.ex. tilldela värdet som returneras till en variabel
function addition(first,second){
    return first+second
}

let result = addition(5,6)
console.log(result)
result = addition("OOO","III")
console.log(result)
```