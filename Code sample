from getpass import getpass


class CRM:
#Create a class to create and store the databases in
  def __init__(self):
    self.database = {}
    self.users = {}
#Input a pateint's info
  def Patient_CRM(self,name, symptoms):
    if name in self.database:
      self.database[name]+= symptoms[0].split(',')
    else:
      self.database[name] = symptoms[0].split(',')

    list(set(self.database[name]))
#Create an account for security
  def create_account(self,user,password):
    self.users[user] = password
#Display a patient by searching their names
  def display_patient(self, user, password, name):
    if password == self.users[user]:
      print(self.database[name])


def main():
  table = CRM()

  # Input 1 to create an account
  while True:
    Log_In = input("Create or Sign In ( 1 or 2) ")
    if Log_In == '1':
      username = input("Enter Username ")
      pass_key = getpass("Enter Password")
      table.create_account(username,pass_key)
      Log_In = input("Now Please Sign In by pressing 2 ")
    #Input 2 to Log In to existing account
    if Log_In == '2':
      Log_In_Username = input('Enter Username ')
      Log_In_Password = getpass("Password")
      if Log_In_Username not in table.users:
        print("Username not found")

      elif Log_In_Password != table.users[Log_In_Username]:
        print("Incorrect Password")
        # resets everthing if username or password is incorrect, goes back to the log in
      else:
        break

    if Log_In != '1' and Log_In != '2':
        print("Invalid choice. Please enter 1 or 2 ")


  while True:
    # three options, add, display, and exit
    print("\nOptions:")
    print("1. Add Patient")
    print("2. Display Patients")
    print("3. Exit")
    choice = input("Enter your choice (1/2/3): ")

    # 1 is for entering the patient's name and symptoms
    if choice == '1':
        name = input("Enter patient name: ")
        symptoms = input("Enter patient symptoms: ")

        table.Patient_CRM(name,[symptoms])
    #2 is for displayong the patients info
    elif choice == '2':
      name = input("Enter patient name:  ")
      if name not in table.database:
        print("Patient not found")
      else:
        table.display_patient(username,pass_key,name)
    #3 is to exit the screen
    elif choice == '3':
      print("Exiting CRM. Goodbye!")
      break

    else:
      print("Invalid choice. Please enter 1, 2, or 3.")



#Example of input

#Create or Sign In ( 1 or 2)
#Press 1 to create Account
#Enter Username
#Enter Password

#Now Please Sign In by pressing 2
#Press 2

#Enter same Username and Password

#Enter your choice of options(1/2/3)
# Add Patient to data base before displaying him
# Add Symptoms in a format such as, with no spaces
# Fever,Headache,Stomach Pain


if __name__ == "__main__":
    main()
