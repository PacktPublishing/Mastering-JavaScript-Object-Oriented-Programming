function Person(name, surname) {
	this.name = name;
	this.surname = surname;

	return { firstName: name, secondName: surname };
}

var johnSmith = new Person("John", "Smith");

console.log(johnSmith.name);				//undefined
console.log(johnSmith.surname);				//undefined
console.log(johnSmith.firstName);			//John
console.log(johnSmith.secondName);			//Smith