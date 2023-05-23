

# [Solid-Principles](https://en.wikipedia.org/wiki/SOLID)

## Object-oriented design 
is a way to design classes together and determine interactions  between them..
Solid-Principles is one of important rules in OO design 
## who wrote it ?
by Robert Martin Author of Clean Code Book
## what is Solid-Principles 
A a set of guidelines that helps us to avoid having a bad design .. however why there is a bad and good design? 🤨
<br />all designs which make its purpose will work.. BUT what about flexibility or maintenance in our System..?
like we built app for paying..we decide we only can accept pay with credits cards ..
## Short-Story
thats good .. our system works well .. after few months we got feedbacks of using our app and our customers 
complaint that they cannot pay with paypal account or Mobile payments 🥺 ...what Shall we do..
go to our system and navigate to class which care about paying and add this..! is it easy ?
we may affect another class correctness repeat integration tesing again !! ..so we need to extend our system to add new features not modifying our System
# lets Start
 S O L I D each char represent a Solution to a specific problem
### S
Single responsibility principle..which mean no class should has more than one  concept ... or simply one object and responsible for one main task like payment in the last EX. "Also payment should be dividend into more than one class"
 <br />Briefly => each class has one concept not more than ONE .. and responsible for one main task
 <br />problem => Fat class will has many tasks if we modify one other may affected and take more time to test or debug
### O
open/close principle which is mean we make class able to adapt with different types of (eg. payment method)
 <br /> so when we need to add new feature it can work with new feature without any conflicts 
 <br />Briefly => each class is open for 'extension' close for 'modification' 
 <br />problem => when adding new feature (eg. paypal payment)  need to change each class deal with payment cycle 
 ### L
 Liskov's Substitution Principle 
 suppose we have rectangle class has its own width , height , get Area function "that's well"
 and i want to inherit from it by square class we will need to change getarea method..
 <br />the problem here is that  i should replace each parent object  with each derived object without any problems "here i want to change getarea implementation"
 <br />Briefly => Dont Change in your parent identification you can extend by adding new methods .. 
  not to override your parent behavioral .. Respect your parents 😅
  ### I
  Interface Segregation Principle is simply you should classify your class hierarchy well to prevent that
  <br /> problem => to make interface has function1 and function2 so every class implement this interface must implement those methods
  what if i(as a implementer class 🧐 ) dont need function2 ?? i will leave it empty .. may causes problems 
  to get rid of that we classify interface like :
  <br />interface1 has function1 and interface2 has function2  
  we (as a implementers classes 😎 ) implement what we need "if i need both So simply => implement Both"
   <br />Briefly => (as interface 😊) be certain that every implementer of me  must need my functions
   ### D
   Dependency Inversion Principle 
   if i(AS ORDER SERVICE CLASS) depend on class PAYMENTSERVICE .. this PAYMENTSERVICE as concrete class may change in coming versions
   so insted of debend on concrete class.. its suggested to debend on interface or abstract class "has little probability to change "
   <br />Briefly => (as  a service class debend on another one 😊) try to debend on abstract or interface classes as you can to reduce regression testing when chnging concrete classes
   



 
 
