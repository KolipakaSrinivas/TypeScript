# TypeScript


* Alternative to Javascript (superset)
* Allow to use strictType
* superts Moeder features like arraow functions let const
* It suport  extra features (generics, interfase,tupls,ect)
* if oldbrosers not support morder js it. typescript complaie morder js to old js it similar balbal
* browser not understand typescript it make clone code before making deploing project need to be complaied


# npm install -g typescript
# To run typescript => tsc filename.ts filename.js 
# if any error open powershall with administer and type :Set-ExecutionPolicy -ExecutionPolicy RemoteSigned enter and y
# if file not created you it crated by own with filenamejs 
# if you craeted => tsc filename.ts filename.js

* It convert const and let  to var its supperts all broswers 


# If we want to complaie auto => tsc filename.ts -w

* main defferent between js and ts. ts use strict .
* if we use string type it always staring it also apply to array and object 
        -- let name = 'srinivas' it always string 


* In typescript we can define type: 'string' 'Number'

        const circ = (diameter: number) => {
            return diameter * Math.PI;
        };

        // console.log(area('hello'));  
        console.log(circ(7.5));


*  typescript strict in  arrays
        
        let names = ['luigi', 'mario', 'yoshi'];

        names.push('toad');
        // names.push(3); error
        // names[1] = 3;  error

        let numbers = [10, 20, 12, 15];

        numbers.push(25); error
        // numbers.push('shaun');error
        // numbers[0] = 'shaun';error

* If create array using mixed string and numbers and other its ok 

        let mixed = ['ken', 4, 'chun-li', 8, 9];

        mixed.push('ryu');
        mixed.push(10);
        mixed[0] = 3;



* typescript in  objects
        let ninja = {
            name: 'mario',
            belt: 'black',
            age: 30
        };

        ninja.age = 40; 
        ninja.name = 'ryu';
        // ninja.age = '30';
        // ninja.skills = ['fighting', 'sneaking'] error

        ninja = {
            name: 'yoshi',
            belt: 'orange',
            age: 40,
            skills: ['running'], error
        };


### we can explact set type in typescript

    let character: string = 'mario';
    let age: number;
    let isLoggedIn: boolean;

    age = 30 //ok
    age ='thirty' //error

    * It works string and boolean

# Array explact
    let ninjas: string[] = []; //ok
    let ninjas: string[]; // error

    ninjas.push('ryu');
    ninjas.push('chun-li');
    console.log(ninjas); //error

# // union types
    let mixed: (string|number|boolean)[] = [];
    mixed.push('hello');
    mixed.push(false);
    mixed.push(20);
    console.log(mixed);

# union types string
    let uid: string|number;


#  objects
    let ninjaOne: object;
    ninjaOne = { name: 'yoshi', age: 30 };

    let ninjaTwo: {
        name: string,
        age: number,
        beltColour: string
    };
    ninjaTwo = { name: 'ken', age: 20, beltColour: 'black' };

### In type Dynamic type (any)

    let age: any = 25;

    age = true;
    console.log(age);
    age = 'hello';
    console.log(age);
    age = { name: 'luigi' };
    console.log(age);

### any Array 

    let mixed: any[] = [];

    mixed.push(5);
    mixed.push('mario');
    mixed.push(false);
    console.log(mixed);

### any object 

    let ninja: { name: any, age: any };
    ninja = { name: 'yoshi', age: 25 };
    console.log(ninja);

    ninja = { name: 25, age: 'yoshi' };
    console.log(ninja);

