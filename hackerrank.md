# **Hackerrank Homework**
<br>
<br>

## **Plus Minus**
<br>

### **Explanation:**
**First I created a varabile called arr that took a array of intergers, then i created a function call plus minus. Inside of that function I assigned '*n*' to equal the arr and its length. After that I created three more varables called postiveNum, negativeNum, zeroNum and I set their values to equal zero. I then used a for loop to get the length of the array I nested an if else statement to set the value for postive negagtive and zero. The logic is if an index/number in the array is greater than 0 give postiveNum an plus 1 the same was done for negative and zero. I then need to make the number divisible by the length of the array that gave me the proper output for example 2/6 gave me 0.33333333. After i figure that out I created three more varables and assigned them to the first three. I did this because I need to pass test case 1 by showing the proper decimal place. I console log pos, neg and zero using a javascript funtion call toFixed to set the proper decimal postion. I then concatinated the varable in one console log.**


<br>

```
let arr = [-4, 3, -9, 0, 4, 1]

function plusMinus(arr) {
    let n = arr.length;
    let postiveNum = 0;
    let negativeNum = 0;
    let zeroNum = 0;
    
    for(let i=0; i < n; i++){
        if(arr[i] > 0){
            postiveNum += 1;
        } else if(arr[i] < 0) {
            negativeNum += 1;
        } else {
            zeroNum += 1;
        }
    }
    let pos = postiveNum / n; 
    let neg = negativeNum / n;
    let zero = zeroNum / n;
    
    console.log(pos.toFixed(6) + "\n" + neg.toFixed(6) + "\n" + zero.toFixed(6));
}
```
<br>
<br>

## **Mini-Max Sum**
<br>

### **Explanation:**
**I first created three varables max, min, and sum, I chose a for loop to  iterate over the length of the array. Starting with max I used an if statement to say if max is less than the current index in the array,  assign array[i] to max this ensures that max will always be equal to the larges sum of the array. I also used a if statement for min the logic is similar, I wrote if min is greater than array[i] assign min that numbner. I found sum by saying sum plus equal the current value. I then created two more varibles maxSum and minSum, my logic here was to say let maxSum equal sum minus min and minSum equal sum minus max. Lastly I console.log to print the sums.**
<br>

```
function miniMaxSum(arr) {
   let max = arr[0];
   let min = arr[0];
   let sum = 0;
   
   for(let i = 0; i < arr.length; i++){
       if(max < arr[i]){
           max = arr[i];
       }
       if(min > arr[i]){
           min = arr[i];
       }
       sum += arr[i];
   }
   let maxSum = sum - min;
   let minSum = sum - max;
   console.log(minSum + " " + maxSum);
}
```

<br>
<br>

## **Time Conversion**
<br>

### **Explanation**
**I created a varible for am pm I used a method call charAt() and set the index to 8 that allows me to manipulate 'a' and 'p' in ampm part of the string for example 12:00:00pm the p is at index 8 and that is what I want to convert when needed. Next I created another variable to store the hours that will be converted. I have three cases I used an if statment alone with a method call substring() to bring it all together. The substring allowed me to manipulate the case that need to be changed. after I workout of the statement I return military hour plus the substring to get proper time conversion.**

```
function timeConversion(s) {
    let amPm = s.charAt(8);
    let militaryHour = "";
    
    if (amPm == "A"){
        if (s.substring(0,2) == "12"){
            militaryHour = "00";
        } 
        else {
            militaryHour = s.substring(0,2);
        }
    } 
    else {
        if (s.substring(0,2) == "12"){
            militaryHour = s.substring(0,2);
        }
        else {
            militaryHour = parseInt(s.substring(0,2), 10) + 12;
        }
    }
    return  militaryHour + s.substring(2,8)
}
```
