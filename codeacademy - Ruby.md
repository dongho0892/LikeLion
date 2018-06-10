# Ruby

## 				1-1 - Introduction to Ruby 

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



## 				2-1 - Control Flow in Ruby 

#### How It Works

* **Control flow** / We can select different outcomes depending on information the user types, the result of a computation, or the value returned by another part of the program. 

````ruby
print "Integer please: "
user_num = Integer(gets.chomp)

if user_num < 0
  puts "You picked a negative integer!"
elsif user_num > 0
  puts "You picked a positive integer!"
else
  puts "You picked zero!"
end
````



#### If + Elsif + Else + end 

*  `true` or `false` 
*  The block of code following an `if`should be indented two spaces. 
* * Ruby doesn't care about **whitespace**  



* "If this expression is true, run this code block; otherwise, run the code after the `else` statement." 
*  The `elsif` statement can add any number of alternatives to an `if`/`else` statement 

```ruby
if x < y  # Assumes x and y are defined
  puts "x is less than y!"
elsif x > y
  puts "x is greater than y!"
else
  puts "x equals y!"
end
```



#### Unless

* you want to use control flow to check if something is *false*, 

````ruby
hungry = false

unless hungry   # false 인 조건 넣기
  puts "I'm writing Ruby programs!"
else
  puts "Time to eat!"
end
````



#### Equal or Not?

* `=` **assignment operator** 					# 할당
* * ​		we assign values to variables



* `==`**comparator** (also called a **relational operator**)     # 같다.
* * ​		means "is equal to." When you type 



* `!=` **comparator**  if two values are *not* equal  		# 같지 않다.



#### Less Than or Greater Than

- Less than: `<`
- Less than or equal to: `<=`
- Greater than: `>`
- Greater than or equal to: `>=`



#### And + Or + Not

* You can also use **logical** or **boolean operators**.
* Ruby has three: and (`&&`), or (`||`), and not (`!`) 

````ruby
true && true # => true
true && false # => false
false && true # => false
false && false # => false
````

* Ruby's `||`is called an **inclusive or** 

````ruby
true || true # => true
true || false # => true
false || true # => true
false || false # => false
````

* the boolean operator **not** (`!`). `!` makes `true` values `false`, and vice-versa. 

````ruby
!true # => false
!false # => true
````



#### Combining Boolean Operators

* **parentheses** (괄호)
* * parentheses are always evaluated before anything outside parentheses. 



#### Nice Work!

- How to use `if`, `else`, and `elsif`
- How to use comparators / relational operators like `==`, `!=`, `<`, `<=`, `>`, and `>=`
- How to use boolean / logical operators like `&&`, `||`, and `!`

````ruby
puts "숫자를 입력해주세요."
puts "첫번째 값"
a = gets.chomp
puts "두번째 값"
b = gets.chomp

if a < b
  print "a is less than b!"
elsif b < a
  print "b is less than a!"
else
  print "b is equal to a!"
end
````

------



## 2-2

#### What You'll Be Building

````ruby
print "Thtring, pleathe!: "
user_input = gets.chomp
user_input.downcase!

if user_input.include? "s"         		# s가 포함되어있는가?
  user_input.gsub!(/s/, "th")			# true 면 s를 th로 바꾸겠다.
else
  puts "Nothing to do here!"
end
  
puts "Your string is: #{user_input}"
````



* `?` evaluate to the boolean values `true` or `false`.) 

* `.gsub!` method, which stands for **g**lobal **sub**stitution.

   ````ruby
  print "뭐든 입력하세요."
  user_input = gets.chomp
  user_input.downcase! 
  # !를 쓰면 기존 것이 바뀌는데
  # !를 안쓰면 그 자리에서 변수에 값을 할당해야만 적용됨.
  
  if user_input.include? "s"
    puts "s가 들어있네요."
    user_input.gsub!(/s/, "th")    
    # gsub!() 사이에 공백 없어야됨! / 슬래시(/값/) 넣어주기
  else
    puts "s가 없습네다."
  end
  
  puts "출력값은 다음과 같습니다. #{user_input}"
   ````

  

------

## 3-1 - Looping with Ruby

#### LOOPS & ITERATORS 

````ruby
# While문
i = 0
while i < 5
  puts i
  i+=1
  # Add your code here!
end
````

````ruby
# Until문   - while과 비슷한 것
counter = 1
until counter > 10
  puts counter
  # Add code to update 'counter' here!
  counter += 1
end
````



#### More Assignment Operators

* You can update a variable with additional assignment operators
* , which include `+=`, `-=`, `*=`, and `/=`. 
* **사용 불가능 : **  `++` and `--`   

-------

#### The 'For' Loop

````ruby
for num in 1..10   # 1..10  : 1부터 10까지 / # 1...10 : 1부터 9까지
    puts num
end
####################################
for num in 1..20
  puts "숫자 : #{num}"
end
````



#### The Loop Method

* The simplest iterator is the `loop` method. 
* The `break` keyword is our Get Out of Jail Free card. 

````ruby
i = 20
loop do
  i -= 1
  print " : #{i}"
  break if i <= 0
end

=begin

Ruby에만 있는 것 
loop do
   ~~
break if (조건)

=end
````



- `next` keyword can be used to skip over certain steps in the loop. 
- * (  Add a line to your loop before your `print`statement. Use the `next` keyword so that you skip to the next iteration if the number `i` is odd. ) - 홀수(odd)일 경우에

```ruby
i = 20
loop do
  i -= 1
  next if i % 2 != 0
  print "#{i}"
  break if i <= 0
end
```



#### Saving Multiple Values

* we can pack multiple values into a single variable using an *array*.  / **square brackets**
* `[1, 2, 3, 4]`



#### The .each Iterator

* `.each` method, which can apply an expression to each element of an object, one at a time.
* `| |` , it's just a placeholder for each element of the object you're using `.each` on.

````ruby
array = [1,2,3,4,5]

array.each do |x|                # do ~ end
  x += 10
  print "#{x}  "
end

array.each { |x|				# {  } 
  x += 10
  print "#{x}  "
}

############
odds = [1,3,5,7,9]

odds.each do |x|
  x *= 2
  print "#{x}  "
# Add your code below!
end
````



#### The .times Iterator

* `.times` method, it can perform a task on each item in an object a specified number of times. 

````ruby
10.times {puts "abc"}
````



#### Looping with 'While'

````ruby
i = 1 				# While do end
while i <= 50
  print i
  i += 1
end
````



#### Looping with 'Until'

````ruby
i = 1				# Util do end
until i > 50 do
  print i
  i += 1
end	
````



#### Looping with 'For'

````ruby
for x in 1..50
  print x
end
````



#### Loop the Loop with Loop

````ruby
count =0
loop do
  puts "Ruby!"
  count += 1
  break if count == 30
end
````



#### Iterating with .times

````ruby
30.times do
  print "Ruby!"
end
````

-------------------

## 3-2

