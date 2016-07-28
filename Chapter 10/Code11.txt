geoModule = (function(mathModule, me) {
	me.calculateSphereVolume = function(radius) {
		return 4*mathModule.PI*mathModule.pow(radius, 2);
	};
	
	return me;
})(Math, geoModule || {});