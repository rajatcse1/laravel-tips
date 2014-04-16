##Problem:  
Pass data `greetings` ans `name` from router to view

##Solution:  
3 ways we can pass as follows:
```
Route::get('/about', function()
{
	/**
	* Way 1: Passing by with function
	* --------------------------------
	return View::make('about')->with(array(
		"greetings" => "hello", 
		"name" => "rajat"
	));
	*/

	/**
	* Way 2: Passing by data veriable
	* --------------------------------
	$data = array(
		"greetings" => "hello", 
		"name" => "ghorai"
	);
	return View::make('about', $data);
	*/

	/**
	* Way 3: Passing by view object
	* --------------------------------
	$view = View::make('about');
	$view -> greetings = "hi";
	$view -> name = "rajat";

	return $view;
	*/
});
```
