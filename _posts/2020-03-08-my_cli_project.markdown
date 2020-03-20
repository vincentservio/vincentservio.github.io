---
layout: post
title:      "My cli project"
date:       2020-03-08 23:39:52 -0400
permalink:  my_cli_project
---


Coming into this project I knew that I would prefer scraping information over using an API. I chose something
that would not only be fun to work on, but would also help me understand how to grab particular
items. I chose to do my something involving my favorite game of all time, NBA 2K.  I began by watching the hour long video tutorial entitled ‘Building a CLI gem walk-through’. Using the IDE
was fairly easy to get started, however due to an inconsistent internet connection I had no
choice but to start my own local environment. Transferring from an IDE to a local environment
had many complications. I had no idea whether I was using it correctly because I had never
used a local environment prior to this


After building my CLI and having fake information pass through, I felt accomplished
having a working CLI and working local environment. But it was time for me to fill it with actual
data. It took a bit of trial and error to get Pry, Nokogiri, and Uri started. Mainly because it was
hard to determine where to put the requires and have it installed correctly. I believe it was due
to my local environment having some missing components. I found it incredibly difficult
grabbing the information that I modeled in the test CLI. Mostly because the site was set up
where the tables had headers that were creating an issue. This pushed me to go to office hours
to get help navigating through the problem. After being able to single out each table most of
the hard work was completed. Unfortunately, the code I used to resolve this problem contained
too much content. However, I felt it was easier for me to understand and explain if needed.
Besides all of that, I only had a little bit of time left to turn it in, and I didn’t want to, nor had the
time to rewrite my entire code. I took the remaining time to make my CLI more user friendly.
Because I feel a lot of the wording was jumbled and spacing made a big difference for the user
experience.

## My Biggest problems
I had problems with Instance variables/methods and Class variables/methods. I believe my problem began with simply not understanding the definition and difference between the two. A Class method is a method that is called on a class while instance methods are called on a classes instance. For example:

```

class Nba2kMe::Player

      def self.all 
         @@all
 
       end
 end 

```
 My .all method is a class method because it made the class function and does not respond to an individual instance of a class. Normally Class methods are initiated with a "self." keyword.  Self represents  
the class so it made it easier to remember how to classify a class method vs. an instance method.  Another major difference is how the methods are called. This class method would be called like this : 

```
Nba2kMe::Playerr.all 
```

Virtually its the same as what we defined earlier which is self.all ((Nba2kMe::Scraper).all). This would return all of the players stored in the @@all array.   So if we tried to call an instance the same way. we would get a NoMethodError. Lets take a look at why 


```

    def list_players
        puts "#########################################"
        puts "### Select the best to beat the best! ###"
        puts "#########################################"
        # @players = Nba2kMe::Player.all
        # @players.each.with_index(1) do |player, x|
            # if x == 1 
            puts "All Around"
            # elsif x == 2
            puts "Shooter"
            # elsif x == 3
            puts "Slasher"
            # elsif x == 4
            puts "Point Guard"
            # elsif x == 5
            puts "Shooting Guard"
            # elsif x == 6
            puts "Small Forward"
            # elsif x == 7
            puts "Power Foward"
            # elsif x == 8
            puts "Center"  
end

```

My interface is constructed by instance method. Because an instance method works with an instance rather than a class, a new instance would have to be created before you can use this method. 



```
Menu = Nba2kMe::CLI.new.menu
```


This is another major difference between the two methods. If a class method is called this way than it will give you the same NOMETHODERROR. 

I struggled writing the definitions of the variables, but i boiled it down to this.

```
@@class_variable 
@instance_variable 

```


Class variables are identified with @@ symbols.The Scope of a Class variable is the entire class. We can access our class variables anywhere in our class: in both class and instance methods. 

```
class Student
#class variable

@@student_count  = 0
 
 def initialize 
 @@student_count +=1 
end 

def self.count
@@student_count

end
end


Student.new 
Student.new 
Student.new 
Student.count 

        # => 3



```

Class variables store data having to do with the entire class .




Instance variables can be read  with a single @ symbol. The scope of an instance variable is the instance itself.  Instance variables are often used to store object instances attributes   .  For example 
```
class Students 

#instance method 

def setname (string) 
@name = string
end 
			
def introduce
puts "hi my name is #{@name}
end 
end
			
			alvin = Students.new
			alvin.setName("alvin")
			alvin.introduce #=> "hi my name is alvin"
			
				theodore = Students.new
			theodore .setName("theodore")
			theodore .introduce #=> "hi my name is theodore "
			
					simon = Students.new
			simon .setname("simon")
			simon .introduce #=> "hi my name is simon "
			
	

```

Each instance would have their own variables of data, specific to the instance of the parent class .  Instance variables can only be accessed inside intance methods , and are not available outside the instance. In other words, a instance variable is defined inside a class and not avaliable outside the class it was created in. attr_accsessor can be helpful to read and write instance variables.  






I worked on this project with another student at a WeWork, however he built his CLI using
an API. So we weren’t much help to each others particular projects, but it definitely helped
when finding bugs in the each others applications while testing.
