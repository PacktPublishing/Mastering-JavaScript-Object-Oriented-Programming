var declaration = "var x = 123;";

function evaluate(code) {
	eval(code);
	return x;
}

console.log(evaluate(declaration));	//result: 123
console.log(x);				//result: undefined