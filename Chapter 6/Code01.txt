function Person(name, surname) {
	this.name = name;
	this.surname = surname;

	return "This is a person";
}

var johnSmith = new Person("John", "Smith");

console.log(johnSmith.name);			//John
console.log(johnSmith.surname);			//Smith