define("geoModule", [], function() {
	var pi = 3.14;

	function circumference(radius) {
  		return 2*pi*radius;
	}

	function circleArea(radius) {
  		return pi*radius*radius;
	}

	return {
  		calculateCircumference:  circumference,
  		calculateCircleArea:   circleArea
	};

});
