# Ruby to JavaScript Worksheet
Read the code in each section, then write the equivalent JavaScript code for the Ruby that is given. Start by writing it out in a text editor or on a piece of paper. Then try running it and tweak your code until it successfully runs with expected output.

Each problem stands alone. Variables from previous problems do not exist.

## Problem Set
1.
```ruby
# Ruby
person_age = 55
ada_age = 2

if person_age < ada_age
   print "This person is younger"
elsif ada_age < person_age
   print "Ada is younger"
else
   print "They’re the same!"
end
```

```javascript
// Javascript
var person_age = 55;
var ada_age = 2;

if (person_age < ada_age) {
  console.log("This person is younger")
} else if (ada_age < person_age) {
  console.log("Ada is younger")
} else {
  console.log("They're the same!")
};
```

2.
```ruby
# Ruby
pet = "cat"
food = "ice cream"

if pet == "cat"
   print "here kitty"
elsif pet == "dog"
   print "woof"
else
   print "some other sound"
end

if food == "broccoli"
   print "eh."
elsif food == "ice cream"
   print "yum"
end
```

```javascript
//Javascript
var pet = "cat";
var food = "ice cream";

if (pet == "cat") {
  console.log("here kitty")
} else if (pet == "dog") {
  console.log("woof")
} else {
  console.log("some other sound")
};

if (food == "broccoli") {
  console.log("eh.")
} else if (food == "ice cream") {
  console.log("yum")
};
```

3.
```ruby
# Ruby
x = 7
y = 7

if x > y || x == y
   if x > y
      print "x is bigger"
   else
      print "x = y"
   end
else
   print "y is bigger"
end
```

```javascript
// Javascript
var x = 7;
var y = 7;

if (x >= y) {
  if (x > y) {
    console.log("x is bigger")
  } else {
    console.log("x = y")
  };
} else {
  console.log("y is bigger")
};
```

4.
```ruby
# Ruby
2.times do
  puts "dance"
end
```

```javascript
//Javascript
for (var i = 0; i < 2; i++) {
  console.log("dance")
};
```

5.
```ruby
10.times do |i|
  puts i
end
```

```javascript
// Javascript
for (var i = 0; i < 10; i++) {
  console.log(i)
};
```

6.
```ruby
# Ruby
3.times do
  puts "coding!"
end
puts "fun!"
```
```javascript
//Javascript

for (var i=0; i < 3; i++) {
  console.log("coding!")
};
console.log("fun!");
```



7.
```ruby
# Ruby
5.times do |x|
  puts "#{x} chicken(s)"
end
```

```javascript
// Javascript
for (var i=0; i<5; i++) {
  console.log(i + " chicken(s)")
};
```


8.
```ruby
# Ruby
10.times do |i|
  puts i * i
end
```

```javascript
// Javascript
for (var i=0; i < 10; i++) {
  console.log(i * i)
};
```

9.
```ruby
# Ruby
(1..5).each do
  puts "hello!"
end
```
```javascript
// Javascript
for (var i=1; i < 6; i++) {
  console.log("hello!")
};
```

10.
```ruby
# Ruby
(1..3).each do |i|
  puts "#{i} animals(s)"
end
```

```javascript
// Javascript
for (var i = 1; i < 4; i++) {
  console.log(i + " animals(s)")
};
```

11.
```ruby
(1..3).each do |i|
  puts i * i
end
```
```javascript
// Javascript
for (var i = 1; i < 4; i++) {
  console.log(i * i)
};
```
12.
```ruby
total = 0

(1..3).each do |i|
  total = total + i
end

puts total
```
```javascript
// Javascript

var total = 0;

for (var i = 1; i < 4; i++) {
  total += i
};

console.log(total);
```


13.
```ruby
(1..10).each do |x|
  if x == 5
    puts "You got a winner!"
  end
end
```
```javascript
// Javascript
for (var x = 1; x < 11; x++) {
  if (x == 5) {
    console.log("You got a winner!")
  };
};
```


14.
```ruby
i = 0

while i < 3
  puts “hi”
  i = i + 1
end
```
```javascript
// Javascript
var i = 0;
while (i < 3) {
  console.log("hi");
  i++;
};
```
15.
```ruby
i = 0

while i < 3
  puts “hi”
  i = i + 1
end

puts "bye"
```
```javascript 
// Javascript


var i = 0;
while (i < 3) {
  console.log("hi");
  i++;
};

console.log("bye");
```


16.
```ruby
i = 0

while i < 3
  i += 1
  puts i
end
```
```javascript
// Javascript
var i = 0;
while (i < 3) {
  i++;
  console.log(i);
};
```
17.
```ruby
x = 5
i = 0

while i < 3
  x = x + 1
  i = i + 1
end

puts x
```
```javascript
// Javascript
var x = 5;
var i = 0;
while (i < 3) {
  x++;
  i++;
};
console.log(x);
```
18.
```ruby
i = 3

while i > 0
  puts "ada!"
  i = i - 1
end
```
```javascript
// Javascript
var i = 3;
while (i > 0) {
  console.log("ada!");
  i--;
};
```

19.
```ruby
cars = ["old", "new", "used"]
cars.each do |car|
  puts car
end
```
```javascript
// Javascript
var cars = ["old", "new", "used"];

for (var i=0; i < cars.length; i++) {
  console.log(cars[i])
}
```
20.
```ruby
fruits = ["banana", "apple", "kiwi"]
fruits.each do |fruit|
  puts "I love " + fruit + "!"
end
```
```javascript
// Javascript
var fruits = ["banana", "apple", "kiwi"];

for (var i=0; i < fruits.length; i++) {
  console.log("I love " + fruits[i] + "!");
};
```
21.
```ruby
total = 0
values = [4, 6, 2, 8, 11]

values.each do |value|
    total = total + value
end

puts total
```
```javascript
// Javascript
var total = 0;
var values = [4, 6, 2, 8, 11];

for (var i=0; i < values.length; i++) {
  total += values[i];
};

console.log(total);
```
22.
```ruby
values = [8, 5, 3, 10, 14, 2]
values.each do |value|
  if value == 10
    puts "Special case!"
  else
    puts "Regular values like #{value}"
  end
end
```
```javascript
// Javascript

var values = [8, 5, 3, 10, 14, 2];

for (var i=0; i < values.length; i++) {
  if (values[i] == 10) {
    console.log("Special case!");
  } else {
    console.log("Regular values like " + values[i]);
  };
};
```
