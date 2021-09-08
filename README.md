# -The-wheat-rice-and-chessboard-problem
 The wheat/rice and chessboard problem
 https://www.codewars.com/kata/5b0d67c1cb35dfa10b0022c7/solutions/javascript
 
 `
 function squaresNeeded(grains){
    let arr = getArrRice(64)
    return  getNumField( grains, arr )
}

function getArrRice (n){
    let arrRice = []
    let acc = 1
    let pre = 1
    for ( let i = 0; i <=64; i++){
        acc += pre*2
        arrRice.push(pre)
        let buffer = pre
        pre = buffer*2
    }
    console.log('getArrRice')
    console.log(arrRice)
    return arrRice
}

function getNumField (num, arr){
    let answer
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] > num) {
            console.log(arr[i], i)
            answer = i
            break
        }
    }
    console.log(answer)
    return answer
}

squaresNeeded(0)
`
