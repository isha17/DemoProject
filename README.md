# DemoProject
I have created spring boot project. I added the calls of method. If you want to run the program. You can do it. It will give you results on console as well.
As mentioned to write a method to print the value in specifc format, method for printAllAddress, method forprint Address Type,and gcd so created 4 methods in Interface.  

Created an interface JsonReader where provide the declaration of all the methods.
In JsonReaderImpl class define the method body. Actually create a method which read the json file then call three mehtods like- 

1)int highestCommonFactor(int[] numbers) throws Exception;(call added for testing)
2) String printAllAddress(List<HashMap<String,String>> addList)throws Exception;
3)String printAddressType(String Type)throws Exception;
4)public String prettyPrintAddress(Address address)throws Exception

model- create a Address model class
but not in a model package) take in same package. I took all classes in one folder due to system error do not want to lost it.

****************
DemoApplication.class is a main method class. WHich calls the json read method->readJsonTagNode
I did not add the @Autowired configuration . Now created directly instance of inplemented class.
**************

*******************
void readJsonTagNode(JsonNode tagsNode)throws Exception;->

method read the data and segregate the  logic to read the nodes on the basis of address type. I was aasuming, as some key jsontag was not present or null in some 
address, if key is null then does not call the get method to get the json value to avoid the null pointer exception.This method is mainly used to read the json file 
data and add in a address object property. 
*******************

*****************
int highestCommonFactor(int[] numbers) throws Exception->
This mehtod provide the highestCommonFactorof any integer array , which call one private method ,which gets gcd of 2 values and continues this process for all the array.
Call thismethos and provide int array in readJsonTagNode methos to show the results at runtime.
***********************

***************
String printAllAddress(List<HashMap<String,String>> addList)throws Exception;->
it returns all the json address of a file. Currently I add a call this method from readJsonTagNode method to show the results at runtime.
********************

******************************
public String prettyPrintAddress(Address address)throws Exception->
As json file have three types of address and some conditions mentioned, so applied that for desired results. And return thestring value and also add the address in a list of address.
************************************

************************
String printAddressType(String Type)throws Exception;->
This mehtod is added to print spefic address type
**************

As mentioned, My system is not working properly and earlier in call. I infomed that I did not worked on spring boot. I choosed this because of less configuration required in spring boot.
I did not added junit test cases.Because system is suddendly shut down automatically. I wanted to delivered first development logic code, so i ll not be lost code.

You can run the code , if run the main method(for this time) and give the input result in readJsonTagNode method.
