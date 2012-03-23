!SLIDE title-slide

# Let's make Ruby better! #

(What Rubyists should steal from Haskell and Clojure)


!SLIDE ralph

<img src="ralph.png">



!SLIDE center
.notes mailing list joke

I'm scared right now.


!SLIDE

# I have a dirty secret.


!SLIDE

# I'm going to make it up to you.


!SLIDE

# Comprehensions


!SLIDE code center medcode

# How Ruby eats lunch:

    @@@ ruby
    foods.each { |food| eat(food) }


!SLIDE code center bigcode

## Sadly, we cannot eat thusly:

    @@@ ruby
    foods.each(&:eat)


!SLIDE code center

## Coffeescript eats our lunch:

    @@@ coffeescript
    eat food for food in foods

!SLIDE code

## Ruby gets health conscious:

    @@@ ruby
        foods.each do |food|
          eat(food) if food != 'chocolate'
        end

!SLIDE code smallcode

## Coffeescript is lean and mean:

    @@@ coffeescript
    eat food for food in foods if food inst 'chocolate'
