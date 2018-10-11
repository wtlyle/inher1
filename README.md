class Car {
    constructor(color, make, model, year , time, signal, speed){
        this.color = color
        this.make = make
        this.model= model
        this.year = year
        this.time = time
        this.lights = this.lights()
        this.signal = signal
        this.turn = this.turn()
        this.speed = 0
    }

    lights(){
        if (this.time === "night") {
            console.log("Lights are on");
            return true
        } else {
            console.log("Lights are off");
            return false
        }
    }
    turn(){
        if (this.signal === "right") {
            console.log("Right Turn Signal");
            return 'Right Turn'
        } else if (this.signal === "left"){
            console.log("Left Turn Signal");
            return 'Left Turn'
        } else {
            console.log("Going Strait");
            return "Strait"
        }
    }
    acceleration(){
        this.speed += 10
    }
    brake(){
        this.speed -= 7
    }


}
let myCar = new Car ("black", "Ford", "Ranger", "1999", "night", "right")
// console.log(myCar.acceleration());
// acceleration(myCar)


// Story: As a programmer, I can tell how many wheels a car has; default is four.
myCar.wheels = 4
// console.log(myCar);
// Story: As a programmer, I can make a Tesla car.
// Hint: Create an variable called myTesla which is of class Tesla which inherits from class Car.
class Tesla extends Car {
    constructor(color, model, year){
    super(color, "Tesla", model, year)
    }

}
let myTesla = new Tesla ("green", "Model S", "2000")
let myTesla1 = new Tesla ("green", "Model S", "2017")
myTesla.acceleration();
myTesla.brake();
// console.log(myTesla);
// console.log(myTesla1);
// Story: As a programmer, I can make a Tata car.
class Tata extends Car {
    constructor(color, model, year){
    super(color, "Tata", model, year)
    }
    acceleration(){
        this.speed += 2
    }
    brake(){
        this.speed -= 1.5
    }

}

let myTata = new Tata ("orange", "Indgo", "2004")
let myTata1 = new Tata ("black", "Indgo", "2005")

myTata.acceleration();
myTata.brake();

// console.log(myTata);
// console.log(myTata1);


// Story: As a programmer, I can make a Toyota car.

class Toyota extends Car {
    constructor(color, model, year){
    super(color, "Toyota", model, year)
    }
    acceleration(){
        this.speed += 7
    }
    brake(){
        this.speed -= 5
    }
}
let myToyota = new Toyota ("silver", "Camery", "2002")
let myToyota1 = new Toyota ("silver", "Camery", "2004")

myToyota.acceleration();
myToyota.brake();
// console.log(myToyota);
// console.log(myToyota1);



var myCars = [];
myCars.push (myToyota, myToyota1, myTata, myTata1, myTesla, myTesla1);
console.log(myCars);

function compare (a, b) {
  const modelA = a.model;
  const modelB = b.model;
  let comparison = 0;
  if (modelA > modelB) {
    comparison = 1;
} else if (modelA < modelB) {
    comparison = -1;
  }
  return comparison;
}

console.log(myCars.sort(compare));

function compareYear (a, b) {
  const yearA = a.year;
  const yearB = b.year;
  let comparison = 0;
  if (yearA > yearB) {
    comparison = 1;
} else if (yearA < yearB) {
    comparison = -1;
  }
  return comparison;
}
console.log(myCars.sort(compareYear));

// Story: As a programmer, I can tell which model year a vehicle is from. Model years never change.
// Hint: Make model year part of the initialization.

//put in the original object

// Story: As a programmer, I can turn on and off the lights on a given Car.
// Hint: Create method(s) to allow programmer to turn lights on and off. Which class are the methods in?


//
// Story: As a programmer, I can determine if the lights are on or off. Lights start in the off position.
//
// Story: As a programmer, I can signal left and right. Turn signals starts off.
//
// Story: As a programmer, I can determine the speed of a car. Speed starts at 0 km/h.
//
// Story: As a programmer, I can speed my Teslas up by 10 per acceleration.
//
// Story: As a programmer, I can slow my Teslas down by 7 per braking.
//
// Story: As a programmer, I can speed my Tatas up by 2 per acceleration.
//
// Story: As a programmer, I can slow my Tatas down by 1.25 per braking.
//
// Story: As a programmer, I can speed my Toyotas up by 7 per acceleration.
//
// Story: As a programmer, I can slow my Toyotas down by 5 per braking.
//
// Story: As a programmer, I can call upon a car to tell me all it's information.
// Hint: Implement carInfo method on one or more classes. You can call a super class's carInfo with super.
//
// Story: As a programmer, I can keep a collection of two of each kind of vehicle, all from different years.
// Hint: Create two of each vehicles, all from different model years, and put them into an Array.
//
// Story: As a programmer, I can sort my collection of cars based on model year.
//
// Story: As a programmer, I can sort my collection of cars based on model.
// Hint: Sort based on class name.
//
// Story: As a programmer, I can sort my collection of cars based on model and then year.
//
//
//
