# AddressBook
Creating an address book in JavaScript

// define some variables as contacts
var bob = {
    firstName: "Bob",
    lastName: "Jones",
    phoneNumber: "(650) 777-7777",
    email: "bob.jones@example.com"
};

var mary = {
    firstName: "Mary",
    lastName: "Johnson",
    phoneNumber: "(650) 888-8888",
    email: "mary.johnson@example.com"
};
//create an array with each contact in it
var contacts = [bob, mary];

function printPerson(person) {
    console.log(person.firstName + " " + person.lastName);
}
//create a function that defines a variable thats the length of how many contacts are in the array, then print the names of the contacts
function list() {
	var contactsLength = contacts.length;
	for (var i = 0; i < contactsLength; i++) {
		printPerson(contacts[i]);
	}
}

/*Create a search function
then call it passing "Jones"*/

var search = function (lastName) {
    var contactsLength = contacts.length;
    for (var i = 0; i < contactsLength; i++) {
		if (lastName === contacts[i].lastName) {
		    printPerson(contacts[i]);
	}
}
}
search("Jones");

//a different way to add a contact, create a function with the parameters of each of the contact objects
function add(firstName, lastName, phoneNumber, email) {
    var newContact = {
    firstName: firstName,
    lastName: lastName,
    phoneNumber: phoneNumber,
    email: email
    }
    //add a new contact to the array with this code
    contacts[contacts.length] = newContact;
}
//call the function above and add each to whatever parameters you listed above
add("mike", "ferger", 123, "bla@gmail.com");
//call the list function to just print the contacts by using the contacts array since you added a new entry to the array
list(contacts);
