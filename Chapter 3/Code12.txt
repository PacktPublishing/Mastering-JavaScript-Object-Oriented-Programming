var person = { 
	name: "John", 
	surname: "Smith",
	get fullName() { return this.name + " " + this.surname; },
	email: "john.smith@packtpub.com"
};

console.log(person.fullName); //John Smith

person.fullName = "Mario Rossi";

console.log(person.fullName); //John Smith

