class Developer {
	constructor(skills, benefits) {
		this.skills = ["programming"].concat(skills);
		this.salary = 40000;
		this.benefits = ["computer"].concat(benefits);
	}
}

class RecruitmentAgency {

	getStaffMember(role, skills, benefits) {
		var member;

		switch(role .toLowerCase()) {
			case "dev":
				member = new Developer(skills, benefits);
				break;
			case "sale":
				member = new Salesman(skills, benefits);
				break;
			case "ba":
				member = new BusinessAnalyst(skills, benefits);
				break;
			default:
				throw new Error("Unable to hire people for the role " + role)
		}

		return member;
	}
}

var agency = new RecruitmentAgency();

var newDevStaffMember = agency.getStaffMember("dev", ["C++", "C#"], ["tablet"]);