A Simple fetcher wrapper javascript
=============================

wraps fetch with class, all you need is provide routes, data, and  callbacks

INSTALLATION
------------

``` npm -i cfetcher ```

after  that in your js file
```javascript

	//imports an object
	import cjsoner from 'cfetcher';

	//adds fetcher behavior
const jsoner = new cjsoner({
	"login2":{
		route:"https://jsonplaceholder.typicode.com/posts",
		method:"get",
   },
});	

//after simply call 
	
	
jsoner.execute("login2", 
	{//provide data for api query
	title: 'foo',
	body: 'bar',
	userId: 1
} , //provide handler for success
	(ok)=>{console.log(ok)},
	//provide handler for error
	(err)=>{console.log(err)});
	
	
```
