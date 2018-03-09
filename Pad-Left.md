# Pad Left - [NPM](https://www.npmjs.com/package/pad-left), [GitHub](https://github.com/jonschlinkert/pad-left)  


Single Responsibility:   
* "Left pad a string with zeros or a specified string.  Fastest implementation."  

On Replication:
* This module would be very easy to implement myself, it might be best not to use this module.  I could code this in under a half an hour then my project would not be dependent on third-party code.  I could also replicate this module's behavior without further dependencies.  Given that their main selling point is being faster than left-pad, the pros don't out-weigh the cons.  My application does not need to pad large strings, or so many strings a minute.  And anyway my app is so far from optimized that faster leftpadding wouldn't make a noticeable difference in performance.

Principle Developer: jonschlinkert

### Index
* [Analysis](#analysis)
  * [Top-Down](#top-down)
  * [Bottom-Up](#bottom-up)
  * [Security](#security)
  * [Competition](#competition)
* [File Structure](#file-structure)  
* [Specs](#specs)  
* [Use Cases](#use-cases)
* [Home](./README.md)

---

## Analysis

This package is the best of it's kind I was able to find.  While it's not too actively maintained, the code is also very simple and still passes it's tests.  The code is also well written and well documented so I would have no trouble hunting down any errors that came from this module.

### Top Down

Community:
1. __Dependent Projects__: 52
2. __Dependencies__: 1
3. __Contributors__: 4
4. __Forks__: 6
5. __Stars__: 31
6. __Curated Lists__: Awesome Micro NPM Packages
7. __Version__: 2.1.0
8. __Releases__: 11
9. __Latest Commit__: March 14, 2017
10. __Downloads Last Month__: 124,085
11. __Open Issues__: 0
12. __Open Pull Requests__: 0
13. __License__: MIT


### Bottom Up

The Code:
1. __Ease of Use__: high
2. __Documentation__: good
2. __Differentiation__: faster 
3. __Maintenance__: unmaintained, but not relevant for such a small package
4. __Project Scope__: Clear, simple, well-stated
5. __Complaints__: no open issues. Just the bigger questions of why not to write it myself
6. __Support__: not relevant with no complaints
7. __Code__: clear and well-written.  I have no trouble understanding it or navigating it

### Security

The source code in this module poses very little risk.  While it's not very actively maintained, and does not have a large group of contributors it's also small and simple enough that this isn't that big of an issue.

But it does have one dependency that could be a vulnerability.  I haven't assessed this one yet.

I can imagine this package posing a risk if someone were to get hold of the maintainer's account and messed with the padding.  They could either have the function pad with a dangerous regular expression, or simply make it pad by more than I want.  Either way they could crash my system, or open dangerous vulnerabilities.


### Competition

There is only one major competitor: The Infamous Left-Pad.  Apparently this one is faster.


[TOP](#index)

---

## File Structure

```
pad-left
|
+-- /benchmark
|	+-- /code
|	|	: Many ways to left pad a string
|	+-- /fixtures
|	|	: Test cases
|	+-- index.js
|	|	: Runs the benchmark tests and outputs the results
|	+-- node-*.md
|		: Outputs from the benchmark tests
|
+-- .*
|		: A whole lot of configuration files
|
+-- LICENSE
|
+-- README.md
|	: Title, stats
|	: The module's behavior, and a link to a related module
|	: Install instructions
|	: Usage instructions
|	: Benchmarking against the infamous left-pad
|	: More related projects
|	: Contributing Guidelines
|	: How to build the docs with verb
|	: How to run the tests
|	: Author info
|	: License
|
+-- index.js
|	: Requires the repeat-string node module
|	: Exports the pad-left function
|	: Defines and exports the module's functionality
|
+-- package.json
|	: Pretty basic package.json
|
+-- test.js
	: Requires mocha, should, and pad-left
	: Exports nothing
	: Runs test cases for pad-left
```

[TOP](#index)

---

## Specs

```
pad-left: Function
	ARGS: 3
		str: String
			* the string to be left-padded
		num: Number
			* the length of the final string
		ch: String
			* what to pad the string with
	RETURN: String
	BEHAVIOR:
		* returns 'str' with 'ch' repeated to the 
		left until 'str' is 'num' characters long.

```

[TOP](#index)

---

## Use Cases

I don't know of many use cases myself. But it must be a common operation since the left-pad incident is real.

It's probably useful if you're doing protocol compliance.

* CodeWars  
* Entering data in a database  
* Formatting URLs  

[TOP](#index)


___
___
### <a href="http://elewa.education/blog" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/36629698-eb7ed6d0-1959-11e8-9a78-7acd2652186e.png" width="100" height="60"/></a>
