# NRetrofit

A framework for helping developers to make http requests and http responses in a natural and intuitive manner. 

Regarding that on web we are using a lot of json transformations, this project aims to be a useful tool, helping to get data on .net applications. 

In a simple manner, this package and components will transform object instances into requests, and responses into objects instances, with the minimum of code.

All data come from web (webapi, json streams and so on).


Sample sintax 1 - natural usage: 
--------------------------------
SomeRequestClass requestObj;
SomeResponseClass responseObj;
// Gets an object from a request
responseObj = NRetrofit.Get<SomeRequestClass,SomeResponseClass>();
// Puts an object into a request
var result = NRetrofit.Post<SomeRequestClass>(requestObj);

Sample Sintax 2 (by using extra Extended methods): 
--------------------------------
Customer cus = new Customer();
cus.Name = "test";
cus.Save();
cus.FromWeb(Id:100);

Sample sintax 3 (by using natural Linq with a list response):
--------------------------------
var list = from i in NRetrofit.Get<SomeRequestClass,SomeResponseClass>() where i.Name == 'John' select i;

