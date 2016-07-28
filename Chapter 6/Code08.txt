class Developer {
	constructor(skills, benefits) {
		this.skills = ["programming"].concat(skills);
		this.salary = 40000;
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

class Salesman {
	constructor(skills, benefits) {
		this.skills = ["selling"].concat(skills);
		this.salary = 50000;
		this.benefits = ["computer"].concat(benefits);
	}
}

class RecruitmentAgency {
	constructor() {
		this.objConstructors = {};
	}

	register(role, constructor) {
		this.objConstructors[role] = constructor;
	}

	getStaffMember(role, skills, benefits) {
		var objConstructor =  this.objConstructors[role];
		var member;

		if (objConstructor) member = new objConstructor(skills, benefits);

		return member;
	}
}

var agency = new RecruitmentAgency();

agency.register("dev", Developer);
agency.register("ba", BusinessAnalyst);
agency.register("sale", Salesman);
