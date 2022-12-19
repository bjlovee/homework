# **Hackerrank Homework**
<br>
<br>

## **Explanation**
First I created a varabile called arr that took a array of intergers, then i created a function call plus minus. Inside of that function I assigned '*n*' to equal the arr and its length. After that I created three more varables called postiveNum, negativeNum, zeroNum and I set their values to equal zero. I then used a for loop to get the length of the array I nested an if else statement to set the value for postive negagtive and zero. The logic is if an index/number in the array is greater than 0 give postiveNum an plus 1 the same was done for negative and zero. I then need to make the number divisible by the length of the array that gave me the proper output for example 2/6 gave me 0.33333333. After i figure that out I created three more varables and assigned them to the first three. I did this because I need to pass test case 1 by showing the proper decimal place. I console log pos, neg and zero using a javascript funtion call toFixed to set the proper decimal postion. I then concatinated the varable in one console log.


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