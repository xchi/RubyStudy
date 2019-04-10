# RubyStudy
What?
How?
Why?

##dynamically typed languages
https://railsware.com/blog/2019/01/03/ruby-vs-java-elegance-contra-ubiquity/
In dynamically typed languages, a programmer does not have to define types every time. Ruby doesn’t rely on types at all and cares about methods it needs to call on a given object (the famous duck-typing).

```
class Animal
attr_accessor :name
end

class Desk
attr_accessor :name
end

animal = Animal.new
desk = Desk.new
stuff = [animal, desk, animal, desk]
```

It’s absolutely fine in Ruby. In statically typed languages the both classes would have to have a common interface (another type) or common base class they can both inherit from. What’s more:
```
whatever = stuff.first
print whatever.name 
```
is also fine as long as the object responds to the method called name.

Statically typed languages show better performance at run-time because they check types before running. At the same time, dynamic typing is associated with better project bootstrapping and changes smoothing, which is especially important in the early to middle stages.
