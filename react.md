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
    console.log("Hi");
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

## 4) setTimeout

###### 4) setTimeout using

```javascript
1)  function handleTimeout() {
        console.log("Time out!");
    }

    setTimeout(handleTimeout()); `It will return value imediatelly`

    setTimeout(handleTimeout(), 2000); `It will return value after 2 second`

    setTimeout(() => {
        console.log("More timing out..."); `regular timeout function`
    }, 4000)

```

## 5)props

###### 5)props for 2 componeets

```javascript
  1)`Like this we are giving props to other components`
  function ChildElement(props) {
        return (
            <div>{props.title}</div>
        )
    }

    function App() {
        const title = "Men"

        return (
            <ChildElement title={title} />
        )
    }



    2)`whole props will bee passed "name", "lastname" and "age", this is for not to suffer`
     function App() {

        const expense = [
            {
                name:"shota",
                lastname:"kokila",
                age:20
            }
        ]

        return (
            <ChildElement expense={expense[0]}/>
        )
    }


    function ChildElement (props) {
        return (
            <div>
                <div>{props.expense.name}</div>
                <div>{props.expense.lastname}</div>
                <div>{props.expense.age}</div>
            </div>
        )
    }




    3) `whole props will bee passed "name", "lastname" and "age" with javascript syntax`
     function App() {

        const expense = [
            {
                name:"shota",
                lastname:"kokila",
                age:20
            }
        ]

        return (
            <ChildElement expense={expense[0]}/>
        )
    }


    function ChildElement ({name, lastname, age}) {
        return (
            <div>
                <div>{name}</div>
                <div>{lastname}</div>
                <div>{age}</div>
            </div>
        )
    }
```

## 6) children statement

###### 5) how to use children statement

```javascript
    1)`exactly how to use "children" statement for minimize our code`
    function App() {
  return (
    <div>
      <h1>Using the Wrapper Component</h1>

      <Wrapper>
        <p>This is some content wrapped by the Wrapper component.</p>
        <button>Click me</button>
      </Wrapper>

      <Wrapper>
        <div>
          <h2>Another wrapped content</h2>
          <p>More text here...</p>
        </div>
      </Wrapper>
    </div>
  );
}

    function Wrapper ({ children }) {
        return (
            <div className="wrapper">
                {children}
            </div>
        )
    }
```



## 6) 

###### 5) 

```javascript

```