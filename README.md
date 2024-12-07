# COP2334-1-Extra-Credit-Programming-Challenge-2
This is a GitHub repository link for the second Pearson Programming Challenge from Module 15.

// PersonData and CustomerData Classes

// This program is used to list down the number of customers along with their first and last names, address, phone number, account number, and mailing list status.

#include <iostream> // Includes the iostream library
#include <string> // Includes the string library
using namespace std; // Assume the use of the standard (std) library.

class PersonData; // Declares the PersonData class.
class CustomerData; // Declares the class CustomerData

class PersonData { // This class is used to store the person's first and last name, address, city, state, zip code, and phone number.
private: // Private members of the class.
  string lastName; // Declares a string variable to store the last name.
  string firstName; // Declares a string variable to store the first name.
  string address; // Declares a string variable to store the address.
  string city; // Declares a string variable to store the city.
  string state; // Declares a string variable to store the state.
  string zipCode; // Declares a string variable to store the zip code.
  string phoneNumber; // Declares a string variable to store the phone number.
public:
  PersonData(); // Declares a default constructor.
  PersonData(string, string, string, string, string, string, string); // Declares a constructor with parameters.
  void setLastName(string); // Declares a void function to set the last name.
  void setFirstName(string); // Declares a void function to set the first name.
  void setAddress(string); // Declares a void function to set the address.
  void setCity(string); // Declares a void function to set the city.
  void setState(string); // Declares a void function to set the state.
  void setZipCode(string); // Declares a void function to set the zip code.
  void setPhoneNumber(string); // Declares a void function to set the phone number.
  string getLastName(); // Declares a string function to get the last name.
  string getFirstName(); // Declares a string function to get the first name.
  string getAddress(); // Declares a string function to get the address.
  string getCity(); // Declares a string function to get the city.
  string getState(); // Declares a string function to get the state.
  string getZipCode(); // Declares a string function to get the zip code.
  string getPhoneNumber(); // Declares a string function to get the phone number.
};

class CustomerData : public PersonData { // This class is used to store the customer's account number, mailing list status, and the customer's data.
private: // Private members of the class.
  int customerNumber; // Declares an integer variable to store the customer number.
  bool mailingList; // Declares a boolean variable to store the mailing list status.
public: // Public members of the class.
  CustomerData(); // Declares a default constructor.
  CustomerData(string, string, string, string, string, string, string, int, bool); // Declares a constructor with parameters.
  void setCustomerNumber(int); // Declares a void function to set the customer number.
  void setMailingList(bool); // Declares a void function to set the mailing list status.
  int getCustomerNumber(); // Declares an integer function to get the customer number.
  bool getMailingList(); // Declares a boolean function to get the mailing list status.
};

PersonData::PersonData() { // This is the default constructor.
  lastName = ""; // Sets the last name to an empty string.
  firstName = ""; // Sets the first name to an empty string.
  address = ""; // Sets the address to an empty string.
  city = ""; // Sets the city to an empty string.
  state = ""; // Sets the state to an empty string.
  zipCode = ""; // Sets the zip code to an empty string.
  phoneNumber = ""; // Sets the phone number to an empty string.
}

PersonData::PersonData(string l, string f, string a, string c, string s, string z, string p) { // This is the constructor with parameters for the PersonData class.
  lastName = l; // Sets the last name to the parameter l.
  firstName = f; // Sets the first name to the parameter f.
  address = a; // Sets the address to the parameter a.
  city = c; // Sets the city to the parameter c.
  state = s; // Sets the state to the parameter s.
  zipCode = z; // Sets the zip code to the parameter z.
  phoneNumber = p; // Sets the phone number to the parameter p.
}

void PersonData::setLastName(string l) { // This function sets the last name.
  lastName = l; // Sets the last name to the parameter l.
}
void PersonData::setFirstName(string f) { // This function sets the first name.
  firstName = f; // Sets the first name to the parameter f.
}
void PersonData::setAddress(string a) { // This function sets the address.
  address = a; // Sets the address to the parameter a.
}
void PersonData::setCity(string c) { // This function sets the city.
  city = c; // Sets the city to the parameter c.
}
void PersonData::setState(string s) { // This function sets the state.
  state = s; // Sets the state to the parameter s.
}
void PersonData::setZipCode(string z) { // This function sets the zip code.
  zipCode = z; // Sets the zip code to the parameter z.
}
void PersonData::setPhoneNumber(string p) { // This function sets the phone number.
  phoneNumber = p; // Sets the phone number to the parameter p.
}
string PersonData::getLastName() { // This function gets the last name.
  return lastName; // Returns the last name.
}
string PersonData::getFirstName() { // This function gets the first name.
  return firstName; // Returns the first name.
}
string PersonData::getAddress() { // This function gets the address.
  return address; // Returns the address.
}
string PersonData::getCity() { // This function gets the city.
  return city; // Returns the city.
}
string PersonData::getState() { // This function gets the state.
  return state; // Returns the state.
}
string PersonData::getZipCode() { // This function gets the zip code.
  return zipCode; // Returns the zip code.
}
string PersonData::getPhoneNumber() { // This function gets the phone number.
  return phoneNumber; // Returns the phone number.
}
CustomerData::CustomerData() { // This is the default constructor.
  customerNumber = 0; // Sets the customer number to 0.
  mailingList = false; // Sets the mailing list status to false.
}

CustomerData::CustomerData(string l, string f, string a, string c, string s, string z, string p, int cn, bool ml) : PersonData(l, f, a, c, s, z, p) { // This is the constructor with parameters for the CustomerData class.
  customerNumber = cn; // Sets the customer number to the parameter cn.
  mailingList = ml; // Sets the mailing list status to the parameter ml.
}
void CustomerData::setCustomerNumber(int cn) { // This function sets the customer number.
  customerNumber = cn; // Sets the customer number to the parameter cn.
}
void CustomerData::setMailingList(bool ml) { // This function sets the mailing list status.
  mailingList = ml; // Sets the mailing list status to the parameter ml.
}
int CustomerData::getCustomerNumber() { // This function gets the customer number.
  return customerNumber; // Returns the customer number.
}
bool CustomerData::getMailingList() { // This function gets the mailing list status.
  return mailingList; // Returns the mailing list status.
}

int main() { // The main function.
  CustomerData customer1("Grady", "Charles", "333 E WonderView Ave", "Estes Park", "CO", "805174", "303-7630", 237, true); // Creates a CustomerData object called customer1 with the given values.
  cout << "Customer 1: " << endl; // Prints a message to the console for the first customer.
  cout << "Last Name: " << customer1.getLastName() << endl; // Prints the last name of customer1 to the console.
  cout << "First Name: " << customer1.getFirstName() << endl; // Prints the first name of customer1 to the console.
  cout << "Address: " << customer1.getAddress() << endl; // Prints the address of customer1 to the console.
  cout << "City: " << customer1.getCity() << endl; // Prints the city of customer1 to the console.
  cout << "State: " << customer1.getState() << endl; // Prints the state of customer1 to the console.
  cout << "Zip Code: " << customer1.getZipCode() << endl; // Prints the zip code of customer1 to the console.
  cout << "Phone Number: " << customer1.getPhoneNumber() << endl; // Prints the phone number of customer1 to the console.
  cout << "Customer Number: " << customer1.getCustomerNumber() << endl; // Prints the customer number of customer1 to the console.
  cout << "Mailing List: " << customer1.getMailingList() << endl;
  cout << endl; // Prints a newline to the console for formatting the mailing list status.
  CustomerData customer2("Jackson", "Johnny", "22 Jump St", "Los Angeles", "CA", "90632", "213-0802", 348, false); // Creates a CustomerData object called customer2 with the given values.
  cout << "Customer 2: " << endl; // Prints a message for the second customer to the console.
  cout << "Last Name: " << customer2.getLastName() << endl; // Prints the last name of customer2 to the console.
  cout << "First Name: " << customer2.getFirstName() << endl; // Prints the first name of customer2 to the console.
  cout << "Address: " << customer2.getAddress() << endl; // Prints the address of customer2 to the console.
  cout << "City: " << customer2.getCity() << endl; // Prints the city of customer2 to the console.
  cout << "State: " << customer2.getState() << endl; // Prints the state of customer2 to the console.
  cout << "Zip Code: " << customer2.getZipCode() << endl; // Prints the zip code of customer2 to the console.
  cout << "Phone Number: " << customer2.getPhoneNumber() << endl; // Prints the phone number of customer2 to the console.
  cout << "Customer Number: " << customer2.getCustomerNumber() << endl; // Prints the customer number of customer2 to the console.
  cout << "Mailing List: " << customer2.getMailingList() << endl;
  cout << endl; // Prints a newline to the console for formatting the mailing list status.
  CustomerData customer3("Andrews", "Nicholas", "634 Cambridge Rd", "New York", "NY", "53170", "212-3456", 789, true); // Creates a CustomerData object called customer3 with the given values.
  cout << "Customer 3: " << endl; // Prints a message for the third customer to the console.
  cout << "Last Name: " << customer3.getLastName() << endl; // Prints the last name of customer3 to the console.
  cout << "First Name: " << customer3.getFirstName() << endl; // Prints the first name of customer3 to the console.
  cout << "Address: " << customer3.getAddress() << endl; // Prints the address of customer3 to the console.
  cout << "City: " << customer3.getCity() << endl; // Prints the city of customer3 to the console.
  cout << "State: " << customer3.getState() << endl; // Prints the state of customer3 to the console.
  cout << "Zip Code: " << customer3.getZipCode() << endl; // Prints the zip code of customer3 to the console.
  cout << "Phone Number: " << customer3.getPhoneNumber() << endl; // Prints the phone number of customer3 to the console.
  cout << "Customer Number: " << customer3.getCustomerNumber() << endl; // Prints the customer number of customer3 to the console.
  cout << "Mailing List: " << customer3.getMailingList() << endl;
  cout << endl; // Prints a newline to the console for formatting the mailing list status.
  CustomerData customer4("Montaque", "Thomas", "678 Caroline Ave", "Portland", "OR", "3365", "503-4321", 233, false);
  cout << "Customer 4: " << endl; // Prints a message for the fourth customer to the console.
  cout << "Last Name: " << customer4.getLastName() << endl; // Prints the last name of customer4 to the console.
  cout << "First Name: " << customer4.getFirstName() << endl; // Prints the first name of customer4 to the console.
  cout << "Address: " << customer4.getAddress() << endl; // Prints the address of customer4 to the console.
  cout << "City: " << customer4.getCity() << endl; // Prints the city of customer4 to the console.
  cout << "State: " << customer4.getState() << endl; // Prints the state of customer4 to the console.
  cout << "Zip Code: " << customer4.getZipCode() << endl; // Prints the zip code of customer4 to the console.
  cout << "Phone Number: " << customer4.getPhoneNumber() << endl; // Prints the phone number of customer4 to the console.
  cout << "Customer Number: " << customer4.getCustomerNumber() << endl; // Prints the customer number of customer4 to the console.
  cout << "Mailing List: " << customer4.getMailingList() << endl;
  cout << endl; // Prints a newline to the console for formatting the mailing list status.
  return 0; // Returns 0 to indicate successful execution of the program.
}
