var IdGenerator = (function() {
	var instance;
	var counter = 0;

	var Constructor = function() {
		if (!instance) {
			instance = this;
		}

		return instance;
	};

	Constructor.prototype.newId = function() {
	return ++counter;
};

	return Constructor;
})();


var g = new IdGenerator();

console.log(g.newId());				//result:		1
console.log(g.newId());				//result:		2

var g1 = new IdGenerator();

console.log(g1.newId());			//result:		3
