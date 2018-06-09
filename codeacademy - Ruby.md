# Ruby

## 				1-1

#### Data Types: Numbers, Strings, Booleans

* never use quotation marks (' or ") with booleans, or Ruby will think you're talking about a string (a word or phrase) instead of a value that can be true or false. 
* It's also important to remember that Ruby is case-sensitive (it cares about capitalization). 

````ruby
my_num =   25  # Add your code here!
my_boolean =  true   # And here!
my_string =  "Ruby"   # Also here.

puts my_num
puts my_boolean
puts my_string
````



#### Variables

*  You can think of a variable as a word or name that grasps a single value.  

````ruby
my_num = 100
# Write code above this line!
puts my_num
````



#### Math

* Addition (`+`) / Subtraction (`-`) / Multiplication (`*`)  
* Division (`/`) / Exponentiation (`**`)  Modulo (`%`)



#### 'puts' and 'print'

* The `print` command just takes whatever you give it and prints it to the screen. 
* `puts` (for "put string") is slightly different:  
* * it adds a new (blank) line after the thing you want it to print. 
* No parentheses or semicolons needed! 

````ruby
print "hello"
puts "hellllo"
puts "hello"
print "hellllo"
````



#### Object - Everything in Ruby is an Object

* everything in Ruby has certain built-in abilities called **methods**.  
* *  methods as "skills" that certain objects have.  
*  The interpreter is the program that takes the code you write and runs it.  
* * **editor**( 코드 입력 ) -> **console**( 결과값 )
* **Methods** are summoned using a `.` 



##### + The '.length' Method

````ruby
my_name = "good person"
my_name_length = my_name.length

puts my_name_length
````

##### + The '.reverse' Method

````ruby
my_name = "good person"
my_name_reverse = my_name.reverse

puts my_name_reverse
````

##### + '.upcase' & '.downcase'

````ruby
my_name = "good person"
my_name_upcase = my_name.upcase
my_name_downcase = my_name.downcase

puts my_name_upcase
puts my_name_downcase
````



#### Single-Line Comments (주석)

````ruby
puts "Eric".length #Eric의 길이를 구하시오.
````

#### Multi-Line Comments

* If you start with `=begin` and end with `=end`, *everything* between those two expressions will be a comment.  

* Don't put any space between the `=` sign and the words `begin` or `end`. 

  ````ruby
  =begin
  you can any write sentences.
  =end
  ````



#### Naming Conventions

* these variables should start with a lowercase letter and words should be separated by underscores, like `counter` and `masterful_method`.  

````ruby
name = "NAME"
````



#### Variables & Data Types

````ruby
my_name = "abc"
my_age = 11
````



#### Strings and String Methods

````ruby
name = "abc"
name.downcase
name.reverse
name.upcase

puts name

name1 = "abc"
name1.downcase.reverse.upcase
puts name1

````

---------------

------------------------



## 				1-2



#### Prompting the User

#### Getting Input

* You may have noticed this weird little line of code  
* `gets` is the Ruby method that *gets* input from the user.  
* `chomp`removes that extra line.  

````ruby
print "What's your first name?"
first_name = gets.chomp
						# 사용자가 이름 입력하기
puts first_name
````

#### Repeat for More Input

````ruby
print "What's your first name?"
first_name = gets.chomp
puts first_name

print "What's your last name?"

last_name = gets.chomp

print "what's your living city?"
city = gets.chomp
print "What's your living state?"
state = gets.chomp.upcase
````



#### Printing the Output

* **string interpolation**    #{variables}

  ````ruby
  print "What's your first name?"
  first_name = gets.chomp
  puts first_name
  
  print "What's your last name?"
  
  last_name = gets.chomp
  
  print "what's your living city?"
  city = gets.chomp
  print "What's your living state?"
  state = gets.chomp.upcase
  
  monkey = "Curious George"
  
  puts "My name is #{first_name} #{last_name} and my living city, state is #{city} #{state}."
  ````

  

  #### Formatting with String Methods

* `capitalize`, the first letter of a string and makes the rest of the letters lower case.  

* `capitalize!`, This modifies the value contained within the variable `변수명`itself. 

````ruby
print "What's your first name? "
first_name = gets.chomp
first_name.capitalize!

print "What's your last name? "
last_name = gets.chomp.capitalize!

print "What city are you from? "
city = gets.chomp
city.capitalize!

print "What state or province are you from? "
state = gets.chomp.upcase!

puts "Your name is #{first_name} #{last_name} and you're from #{city}, #{state}!"

=begin
		What's your first name? abc
		What's your last name? xyz
		What city are you from? ny
		What state or province are you from? wasington
		Your name is Abc Xyz and you're from Ny, WASINGTON!
=end

# ! 사용시,  This modifies the value contained within the variable (변수명) itself.
#  The next time you use the variable answer
#                                         you will get the results of (변수명).capitalize

````



## 				2-1









