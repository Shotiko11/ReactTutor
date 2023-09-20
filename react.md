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

## **2) arrays**

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

## **3) arrays**

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

## **4) setTimeout**

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

## **5)props**

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
```

```javascript
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
```

```javascript
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

## **6) children statement**

###### 6) how to use children statement

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

## **7) onclick event**

###### 7) What should happen when we click "something"

```javascript
`First type of click handler`
    1)const Example = () => {

        const num = 5;

        return (
            <button onClick={() => {
                    console.log("Hello")
                }}></button>
        )
    }
```

```javascript
`second type of click handler`
    2)const Example2 = () => {

        const num = 5

        const clickHandler = () => {
            if(num === 5) {
                console.log("hello")
            }
        }

        return (
            <button onClick={clickHandler} ></button>
        )
    }
```

## **8) useState event**

###### 8) how do we use that useState function?

```javascript
`we can use react hook useState like that, its very useful function(hook)`;
import treact, { useState } from "react";

const [num, setNum] = useState(0);

const handleclick = () => {
  setNum(num + 1);
};

return (
  <div>
    <h1>{num}</h1>

    <button onClick={handleclick}></button>
  </div>
);
```

## **9) input onChange**

###### 9) how to work with onChange listener

```javascript
    `exactly how to use onChange in our code basically`
    1) const Expense = () => {

        const titleHandler = () => {
            console.log("title changed!")
        }


        return (
            <input type="text" onChange={titleHandler} />
        )
    }
```

```javascript
`get value from input, in this example vlaue will be written in console, event.target.value`;
const Expense = () => {
  const titleHandler = (event) => {
    console.log(event.target.value);
  };

  return <input type="text" onChange={titleHandler} />;
};
```

## 10) onChange and useState

###### 10) how to mix onChange and useState together for one target

```javascript
`this will show you same text what you will write inside the input`
const Expense = () => {
  const [value, setValue] = useState("");

  const ChangeHandler = (event) => {
    setValue(event.target.value);
  };

  return (
    <div>
      <input type="text" onChange={ChangeHandler} />

      <h1>{value}</h1>
    </div>
  );
};
```

```javascript
`this will show you same text what you write in input, but only when you click the button`
const Expense = () => {
  const [value, setValue] = useState("");
  const [fase, setfase] = useState(false);

  const getvalue = (e) => {
    setValue(e.target.value);
  };

  return (
    <div>
      <input type="text" onChange={getvalue} />

      <button onClick={() => setfase(!fase)}>Click</button>

      {fase ? <h1>{value}</h1> : null}
    </div>
  );
};
```



# 11) Deep useState

###### 11) how to use useState even better?

```javascript
`here we are giving useState 4 properties which will help us more in the future for minimize the code`
    const Expense = () => {

        const [user, setUser] = useState({
            first: '',
            second:'',
            third:''
        })

            `here, all the info is saved by this--> ...user, and we cna change only first`
        const titleChangeHandler = (event) => {
            setUserInput((prevState) => {
                return {...prevState, first: event.target.value };
            })
    }
```


# 12) 

###### 12) 

```javascript
  function fds = () => {
  const 5 =  das
}
```
