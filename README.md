
## String methods in Javascript 
let mystr = "hi, I am a string";

```bash
console.log(mystr.length)
17

console.log(mystr.slice(1,5)) 
i, I

console.log(mystr.indexOf("am"))
VM5443:1 6
// count starts from 0, spaces are also counted 

let mystr1 = "hi, I am a string am";
console.log(mystr1.lastIndexOf("am"))
18

d = mystr1.replace("hi","bye");
console.log(d);
//bye, I am a string am 

```
### 1. Creating object without new keyword 
Advanced version of arrays 
```bash 
 <script>
            var a = {
               //key: value 
              //property: value
                fname : 'reem',
                lname : 'shaikh',
                age : 20,
                email: 'rtrreem.rchc@gmail.com',

                //array inside object 
                favMovies : ['abcd', 'efgh', 'lkjh'],

                //adding object inside object 
                living :
                {
                   city : 'mumbai',
                   country : 'india'
                },

                salary :  function()   //method
                {
                    return 1000000;
                },

                fullname : function()   //method 
                {
                    return this.fname + " " + this.lname;
                }
            }

            console.log(a.fname);
            console.log(a)
            
            //calling array inside objects 
            console.log(a.favMovies);
            console.log(a.favMovies[0]);  //abcd

            console.log(a.salary());

            console.log(a.fullname());
            //reem shaikh

            //calling object inside object 
            console.log(a.living.city);
</script>

console:
reem
object >

(3) ['abcd', 'efgh', 'lkjh']
0: "abcd"
1: "efgh"
2: "lkjh"
length: 3
[[Prototype]]: Array(0)

abcd
dom.html:25 1000000
reem shaikh
mumbai 
```
### 2. Creating an object and assigning value using new keyword 
```bash
 <script>
          var person = new Object();
          person.firstName = 'reem';
          person.lastName = 'shaikh';
          person.age = 20;

          console.log(person.firstName);
          //can also write it like this 
          //console.log(person['firstName']);
</script>

console:
reem
```
