# React Study

## 1) Class
######1)easy class for example, it will print "name and age"
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


## 2)arrays
###### 2)different example of arrays
```javascript
    const hobbies = ["Sports", "Cooking", "Reading"];

    1)hobbies.push("Working"); `add "Working" at last`

    2)hobbies.map((item) => { item + "!" }) `it will add "!" at the end of each item`

    3)hobbies.map((item) => ({text: item})); `it will add text before value each element`
    
    4)const index = hobbies.findIndex((item) => {
        return item === "Sports";  `daabrunebs "0"-s
    })


```