# React Study

## 1) Class
###### 1) easy class for example, it will print "name and age"
```javascript
class User {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    greet() {
        console.log('Hi');
    }
}

const user1 = new User("Shotiko", 20);
console.log(user1);
```


## 2) arrays
###### 2) different example of arrays
```javascript
    const hobbies = ["Sports", "Cooking", "Reading"];

    1)hobbies.push("Working"); `add "Working" at last`

    2)hobbies.map((item) => { item + "!" }) `it will add "!" at the end of each item`

    3)hobbies.map((item) => ({text: item})); `it will add text before value each element`
    
    4)const index = hobbies.findIndex((item) => {
        return item === "Sports";  `daabrunebs "0"-s
    })


```


## 3) arrays
###### 3) arrays
```javascript
    1) const [firstName, lastName] = ["Shotiko", "Kokilashvili"] `console.log(firstname) will print Shotiko and console.log(lastname) will print kokilashvili`

    2)const user = {
        name: "Shotiko",
        age: 20
      };

      const name = user.name `this will print Shotiko`
      const age = user.age    `this will print 20`

    3) const hobbies = ["Sports", "Cooking"];
        const unitedHobbies = [...hobbbies]
        console.log(unitedHobbies) `it will print Sports and Cooking together for this: ...`

    4) const hobbies = ["Sports", "Cooking"];

       for (const hobby of hobbies) {
            console.log(hobby); `this will print Sports and cooking, it's just a loop`
        }

    5)
```


## 4) 
###### 5) 
```javascript

```