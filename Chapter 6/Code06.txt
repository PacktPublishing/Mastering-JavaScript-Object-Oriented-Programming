class Salesman {
	constructor(skills, benefits) {
		this.skills = ["selling"].concat(skills);
		this.salary = 50000;
		this.benefits = ["computer"].concat(benefits);
	}
}

class BusinessAnalyst {
	constructor(skills, benefits) {
		this.skills = ["analyzing"].concat(skills);
		this.salary = 60000;
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

	hireSalesman() {
		var sm = new Salesman(["communication"], ["smartphone", "car"]);
		this.employees.push(sm);
	}

	hireBusinessAnalyst() {
		var ba = new BusinessAnalyst(["communication", "writing"], ["smartphone", "tablet"]);
		this.employees.push(ba);
	}
}