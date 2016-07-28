function square(n) {
  return n * n;
}

console.log(square(3));			//result: 9

console.log(square("3"));		//result: 9

console.log(square("three"));		//result: NaN
console.log(square(true));		//result: 1
console.log(square({a: 2}));		//result: NaN