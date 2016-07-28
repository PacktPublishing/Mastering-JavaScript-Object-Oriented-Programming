var IdGenerator = (function(){
    var instance;
	 var counter = 0;

    return class {
		 constructor() {
			if (!instance) {
				instance = this;
			}

			return instance;
		 }

		 newId() {
			return ++counter;
		 }
    };
})();
