function SoftwareHouse() {
	this.employees = [];
	
}

SoftwareHouse.prototype.hire = function(dev) {
	this.employees.push(dev);
};

/*
class SoftwareHouse {
	constructor() {
		this.employees = [];
	}

	hire(dev) {
		this.employees.push(dev);
	}
}
*/

var johnSmith = {name: "John", surname: "Smith"};
var lassie = {name: "Lassie", breed: "Collie"};
var table = {type: "round", legsNumber: 1};

var swHouse = new SoftwareHouse();

swHouse.hire(johnSmith);
swHouse.hire(lassie);
swHouse.hire(table);

console.log(swHouse.employees.length);		//result:	3