class Developer {
	constructor(skills, benefits) {
		this.skills = ["programming"].concat(skills);
		this.salary = 40000;
		this.benefits = ["computer"].concat(benefits);
	}
}

class SoftwareHouse {
	constructor() {
		this.employees = [];
	}

	hireDeveloper() {
		var dev = new Developer(["JavaScript"], ["smartphone"]);
		this.employees.push(dev);
	}
}