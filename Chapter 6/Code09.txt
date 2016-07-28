class Developer {
	constructor(skills, benefits) {
		this.skills = ["programming"].concat(skills);
		this.salary = 40000;
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

class BusinessAnalyst {
	constructor(skills, benefits) {
		this.skills = ["analyzing"].concat(skills);
		this.salary = 60000;
		this.benefits = ["computer"].concat(benefits);
	}
}


class DevAgency {
	getStaffMember(skills, benefits) {
		return new Developer(skills, benefits);
	}
}

class SalesAgency {
	getStaffMember(skills, benefits) {
		return new Salesman(skills, benefits);
	}
}

class BusinessAnalystAgency {
	getStaffMember(skills, benefits) {
		return new BusinessAnalyst(skills, benefits);
	}
}

class RecruitmentAgencyAbstractFactory {
	
	constructor() {
		this.agencyFactories = {};
	}

		register(area, agencyFactory) {
		this.agencyFactories[area] = agencyFactory;
	}

	getAgency (area) {
		return new this.agencyFactories[area];
	}
}

var agencyFinder = new RecruitmentAgencyAbstractFactory();

agencyFinder.register("dev", DevAgency);
agencyFinder.register("sales", SalesAgency);
agencyFinder.register("ba", BusinessAnalystAgency);

var devAgency = agencyFinder.getAgency("dev");
var newDevMember = devAgency.getStaffMember(["JavaScript"], ["phone"]);
