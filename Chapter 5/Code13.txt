function Interface(name, methods, properties) {
  "use strict";

  methods = methods || [];
  properties = properties || [];
  
  this.name = name;
  this.methods = [];
  this.properties = [];

  for (let i = 0, len = methods.length; i < len; i++) {
    if (typeof methods[i] !== 'string') {
      throw new Error("Interface constructor expects method names to be passed in as a string.");
    }
    this.methods.push(methods[i]);
  }
  
  for (let i = 0, len = properties.length; i < len; i++) {
    if (typeof properties[i] !== 'string') {
      throw new Error("Interface constructor expects property names to be passed in as a string.");
    }
    this.properties.push(properties[i]);
  }
}


Interface.prototype.isImplementedBy = function(obj) {
  "use strict";
  var methodsLen = this.methods.length;
  var propertiesLen = this.properties.length;
  var currentMember;
  
  if (obj) {
    //check methods
    for (let i = 0; i < methodsLen; i++) {
      currentMember = this.methods[i];
      if (!obj[currentMember] || typeof obj[currentMember] !== "function") {
        throw new Error("The object does not implement the interface " + this.name + ". Method " + currentMember + " not found.");
      } 
    }
    
    //check properties
    for (let i = 0; i < propertiesLen; i++) {
      currentMember = this.properties[i];
      if (!obj[currentMember] || typeof obj[currentMember] === "function") {
        throw new Error("The object does not implement the interface " + this.name + ". Property " + currentMember + " not found.");
      } 
    }
  } else {
    throw new Error("No object to check!");
  }
};

var IHireable = new Interface("IHireable", ["writeCode"], ["name"]);

class SoftwareHouse {
	constructor() {
		this.employees = [];
	}

	hire(dev) {
		IHireable.isImplementedBy(dev);
		this.employees.push(dev);
	}
}