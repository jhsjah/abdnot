
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

## 7. Arrays 
in JS, array is a collection of multiple datatypes of elements.
> collection of elements/ strings/ booleans.
```bash
var arr = [1,"reem",3,4,5.55];
console.log(arr);
```

> Array is a container/ special variable which can hold more than one datatype
Values are stored in indices.
```bash 
 <script>
      var arr = ['reem', 'shaikh', 20, "india"];

      for (var a = 0; a <= 3; a++) {
        document.write(arr[a] + '<br>')
        //0
        //1
        //2
        //3
      }
 </script>

viewport:
reem
shaikh
20
india
```
### Creating Array without new keyword 
```bash 
<script>
      var arr = [ 10, 30, 20, 40];
      var sum = 0;

      for (var a = 0; a <= 3; a++) {
        sum = sum + arr[a]
      }
      
      document.write(sum);
</script>

viewport:
100
```
### Another way to create array using new keyword 
```bash
      var arr = new Array('reem', 'shaikh', 20, 'india')

      for (var a = 0; a <= 3; a++) {
        document.write(arr[a] + '<br>')
      }
```
### Using static value in new keyword:
```bash 
<script>
    //we can add unlimited values in this 
      var arr = new Array();
      arr[0] = 10;
      arr[1] = "reem";
      arr[2] = true;

      for (var a = 0; a <= 2; a++) {
        document.write(arr[a] + '<br>')
      }
</script>
```

### Adding dyanamic values through new keyword 
```bash
<script> 
    var arr = new Array(3);

    for (var a = 0; a < 3; a++) {
        arr[a] = prompt("enter the value");
      }

    for (var g = 0; g < 3; g++) {
        document.write(arr[g] + "<br>");
      } 

</script>

viewport:
reem
100
true
```

## Multidimensional Arrays 
> Array inside array 
```bash 
    <script> 
    var arr = [
        // 0     1      3
        ["reem", 20, "female"], //0
        ["reem", 20, "female"], //1
        ["reem", 20, "female"], //2
        ["reem", 20, "female"]  //3
    ];

    //outer loop (rows)
    for(var a=0; a<4; a++)
    {
        //inner loop (columns)
        for(var b=0; b<4; b++)
        {
            document.write(arr[a][b] + " ");
        }
        document.write("<br>");
    }
    </script>

viewport:
reem 20 female 
reem 20 female 
reem 20 female 
reem 20 female 
```

Presenting it in a table 
```bash 
   <script> 
    var arr = [
        // 0     1      2
        ["reem", 20, "female"], //0
        ["reem", 20, "female"], //1
        ["reem", 20, "female"], //2
        ["reem", 20, "female"]  //3
    ];

document.write("<table border= '1px'>");
    //outer loop (row)
    for(var a=0; a<4; a++)
    {
        document.write("<tr>");
        //inner loop (column)
        for(var b=0; b<3; b++)
        {
            document.write("<td>" + arr[a][b] + "</td>");
        }
        document.write("</tr>");
    }
    document.write("</table>");
    </script>

viewport: //table border is not visible in readme, run this on vscode 

reem	20	female
reem	20	female
reem	20	female
reem	20	female
```

## Array of objects 
> objects inside array

```bash 
 <script>
          var student = [
              {name :'reem', age :20},
              {name :'abcd', age :20},
              {name :'efgh', age :20},
          ];
          console.log(student);
</script>

console:
(3) [{…}, {…}, {…}]0: {name: 'reem', age: 20}1: {name: 'abcd', age: 20}2: {name: 'efgh', age: 20}length: 3[[Prototype]]: Array(0)
```
Printing using for loop 
```bash
 <script>
          var student = [
              {name :'reem', age :20},
              {name :'abcd', age :20},
              {name :'efgh', age :20},
          ];
          console.log(student);

          //printing in a loop
          for(var a=0; a < student.length; a++ )
          {
              document.write(student[a].name + " " + student[a].age + " " + "<br>");
          }
</script>

viewport:
reem 20
abcd 20
efgh 20
