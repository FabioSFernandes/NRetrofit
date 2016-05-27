# NRetrofit

A framework for helping developers to make http requests and http responses in a natural and intuitive manner. 

Regarding that on web we are using a lot of json transformations, this project aims to be a useful tool, helping to get data on .net applications. 

In a simple manner, this package and components will transform object instances into requests, and responses into objects instances, with the minimum of code.

All data come from web (webapi, json streams and so on).


Sample sintax 1 - natural usage: 
--------------------------------
SomeRequestClass requestObj;</br>
SomeResponseClass responseObj;</br>
// Gets an object from a request</br>
responseObj = NRetrofit.Get<<SomeRequestClass,SomeResponseClass>>();</br>
// Puts an object into a request</br>
var result = NRetrofit.Post<<SomeRequestClass>>(requestObj);</br>
</br>
Sample Sintax 2 (by using extra Extended methods): </br>
--------------------------------------------------</br>
Customer cus = new Customer();</br>
cus.Name = "test";</br>
cus.Save();</br>
cus.FromWeb(Id:100);</br>
</br>
Sample sintax 3 (by using natural Linq with a list response):</br>
------------------------------------------------------------------</br>
var list = from i in NRetrofit.Get<<SomeRequestClass,SomeResponseClass>>() where i.Name == 'John' select i;</br>
</br>

