function getFileContent(moduleName) { /*...*/ }

function loadModule(moduleName) {
	var moduleCode = new Function("return " + getFileContent(moduleName));

	return moduleCode();
}