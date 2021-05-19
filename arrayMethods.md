Array Methods


Map

    Returns a new array containing the results of calling a function on every element in this array.

Syntax:
    map((element) => { ... } )
    map((element, index) => { ... } )
    map((element, index, array) => { ... } )

Examples:
    Example 1
        Const array1 = [1,4,9,16]
        Const map1 = array1.map(x => x*2)
            console.log(map1)
                 //output: Array [2,8,18,32]
    Example 2
        Let numbers = [4,9,16,25]
        numbers.map(Math.sqrt)
                //output: numbers = [2,3,4,5]

Reduce

    Apply a function against an accumulator and each value of the array (from left-to-right) as to reduce it to a single value.

Syntax:
    reduce((accumulator, currentValue) => { ... } )
    reduce((accumulator, currentValue, index) => { ... } )
    reduce((accumulator, currentValue, index, array) => { ... } )
    reduce((accumulator, currentValue, index, array) => { ... }, initialValue)

Examples:
    Example1:
        Let array1 = [1,2,3,4]
        const reducer =  (accumulator, currentValue) => accumulator + currentValue;
        console.log(array1.reduce(reducer))
            //output: 10
        console.log(array1.reduce(reducer, 5))
            //output: 15
    Example2:
        Let array = [1,2,3,4]
        array.reduce((acc, c) => acc * c)
            //output: 24


Filter

    Returns a new array containing all elements of the calling array for which the provided filtering function returns true.

Syntax:
    filter((element) => { ... } )
    filter((element, index) => { ... } )
    filter((element, index, array) => { ... } )

Examples:

    Example1:
        const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];
        const result = words.filter(word => word.length > 6);
            console.log(result);
                 //output: Array ['exuberant', 'destruction', 'present']
    Example2:
        var ages = [32, 33, 16, 40];
        function checkAdult(age) {
            return age >= 18;
        }
            Output: [32, 33, 40]


forEach

    Calls a function for each element in the array.
Syntax:
    forEach((element) => { ... } )
    forEach((element, index) => { ... } )
    forEach((element, index, array) => { ... } )

Examples:
    1:
        const array1 = ['a', 'b', 'c'];
        array1.forEach(element => console.log(element));
            // expected output: "a"
            // expected output: "b"
            // expected output: "c"
    2: 
        let words = ['one', 'two', 'three', 'four']
        words.forEach(function(word) {
            console.log(word)
        if (word === 'two') {
            words.shift() //'one' will delete from array
        }
        }) // one // two // four


    console.log(words);  //['two', 'three', 'four']


Sort

    Sorts the elements of an array in place and returns the array.

Syntax:
    // Functionless
    sort()
    // Arrow function
    sort((firstEl, secondEl) => { ... } )
Examples:
    1
        let numbers = [4, 2, 5, 1, 3];
        numbers.sort((a, b) => a - b);
        console.log(numbers);
            // [1, 2, 3, 4, 5]
    2
        const months = ['March', 'Jan', 'Feb', 'Dec'];
        months.sort();
        console.log(months);
            // expected output: Array ["Dec", "Feb", "Jan", "March"]


Slice

    Extracts a section of the calling array and returns a new array.

Syntax
    slice()
    slice(start)
    slice(start, end)
Examples
    1
        const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];
        console.log(animals.slice(2));
            // expected output: Array ["camel", "duck", "elephant"]
    2
        const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];
        console.log(animals.slice(2, 4));
            // expected output: Array ["camel", "duck"]
    3
        console.log(animals.slice(1, 5));
            // expected output: Array ["bison", "camel", "duck", "elephant"]


Pop

    Removes the last element from an array and returns that element.

Syntax
    pop()
    
Examples

    1
        const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];
        console.log(plants.pop());
            // expected output: "tomato"
    2
        var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
        var popped = myFish.pop();
        console.log(myFish); // ['angel', 'clown', 'mandarin' ]
        console.log(popped); // 'sturgeon'


Shift

    Removes the first element from an array and returns that element.

Syntax
    shift()

Examples
    1
        const array1 = [1, 2, 3];
        const firstElement = array1.shift();
        console.log(array1);
            // expected output: Array [2, 3]	
    2
        var fruits = ["Banana", "Orange", "Apple", "Mango"];
        fruits.shift();
             //[“Orange”,”Apple”,”Mango”]



Push

    Adds one or more elements to the end of an array, and returns the new length of the array.

Syntax:
    push(element0)
    push(element0, element1)
    push(element0, element1, ... , elementN)

Examples
    1
        const animals = ['pigs', 'goats', 'sheep'];
        const count = animals.push('cows');
        console.log(count);
            // expected output: 4
        console.log(animals);
            // expected output: Array ["pigs", "goats", "sheep", "cows"]
    2
        let sports = ['soccer', 'baseball']
        let total = sports.push('football', 'swimming')


        console.log(sports)  // ['soccer', 'baseball', 'football', 'swimming']
        console.log(total)   // 4


Unshift

    Adds one or more elements to the front of an array, and returns the new length of the array.

Syntax
    unshift(element0)
    unshift(element0, element1)
    unshift(element0, element1, ... , elementN)

Examples
    1
        const array1 = [1, 2, 3];
        console.log(array1.unshift(4, 5));
            // expected output: 5


        console.log(array1);
            // expected output: Array [4, 5, 1, 2, 3]

    2
        let arr = [4, 5, 6]
        arr.unshift(1, 2, 3)
        console.log(arr);
            // [1, 2, 3, 4, 5, 6]


Includes

    Determines whether the array contains a value, returning true or false as appropriate.

Syntax:
    includes(searchElement)
    includes(searchElement, fromIndex)

Examples

    1:
        const array1 = [1, 2, 3];
        console.log(array1.includes(2));
        // expected output: true
    2:
        const pets = ['cat', 'dog', 'bat'];
        console.log(pets.includes('cat'));
        // expected output: true

indexOf

Returns the first (least) index of an element within the array equal to an element, or -1 if none is found.

Syntax:

    indexOf(searchElement)
    indexOf(searchElement, fromIndex)

Examples:
    1
        const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];
        console.log(beasts.indexOf('bison'));
        // expected output: 1
    2
        const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];
        console.log(beasts.indexOf('giraffe'));
        // expected output: -1


Every

    Returns true if every element in this array satisfies the testing function.

Syntax
    every((element) => { ... } )
    every((element, index) => { ... } )
    every((element, index, array) => { ... } )

Examples
    1
        const isBelowThreshold = (currentValue) => currentValue < 40;
        const array1 = [1, 30, 39, 29, 10, 13];
        console.log(array1.every(isBelowThreshold));
        // expected output: true
    2
        function isNegative(element, index, array) {
        return element < 0;
        }
        const int8 = new Int8Array([-10, -20, -30, -40, -50]);
        console.log(int8.every(isNegative));
        // expected output: true




One: Given a non-empty array of integers, return the result of multiplying the values together in order. Example: [1, 2, 3, 4] => 1 * 2 * 3 * 4 = 24

Let array = [1,2,3,4]
	array.reduce((acc, c) => acc * c)


Two: You will be given an array of all the family members' ages, in any order. The ages will be given in whole numbers, so a baby of 5 months, will have an ascribed 'age' of 0. Return a new array with [youngest age, oldest age, difference between the youngest and oldest age].
	
	Let array = [12,55, 9, 50, 18] 


Three: Sum all the numbers of the array except the highest and the lowest element (the value, not the index!). Example: [ 6, 2, 1, 8, 10 ] => 16 [ 1, 1, 11, 2, 3 ] => 6

//sort
//get rid of index 1 and array.length - 1
//then map

Let array = [122, 3, 55, 20, 12]
array.sort((a,b)=>a-b)
//[3, 12, 20, 55, 122]
array.pop()
	//122
array.shift()
	//3
array.reduce((acc,c) => acc +c)
	//87



	


