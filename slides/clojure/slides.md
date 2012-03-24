!SLIDE mindblown

# Stop! 

# Clojure time.


!SLIDE 

## "Lisp is worth learning for the profound enlightenment experience you will have when you finally get it..." 

--Eric Raymond


!SLIDE mindblown

![mindblown](mblown.gif)


!SLIDE 

# Maybe not that good.

# But pretty close.

!SLIDE

# Functional programming.
## (Highly recommended.)

!SLIDE incremental

# Clojure's functional flavor:

* Programs are composed of functions.
* Functions depend only on their arguments.
* Functions are idempotent.
* Functions have no effect on the world.

!SLIDE 

# Clojure's data types are immutable.

!SLIDE incremental

# Functional/immutable benefits:

* Programs are easy to test.
* Programs are easier to reason about.
* Concurrency is possible.

!SLIDE code center

# Sexps are awesome

    @@@ clojure
    (< 3 4) #=> true
  
    (+ 3 4) #=> 7

    (+ 3 (* 2 3)) #=> 9

!SLIDE medcode

## Sad, sad, sample function

    @@@ clojure
    (defn text-ex-girlfriend [bac]
      (when (> bac 0.06)
        (send-weepy-message)))

!SLIDE incremental

# Easy-peasy syntax

* Remarkably consistent
* No precedence questions
* Smug sense of superiority


!SLIDE code
# Anaphora!

!SLIDE bigcode
    @@@ clojure
    (filter even? (range 10))

!SLIDE medcode yankleft
    @@@ clojure
    (filter 
      (fn [word] (= (count word) 3)) 
      words)

!SLIDE bigcode
    @@@ clojure
    (filter 
      #(= (count %) 3) 
      words)
    
!SLIDE incremental code
# Imagine this in ruby!

    @@@ ruby
    # From this
    def three_letter_words(words)
      words.select { |word| word.length == 3 }
    end

    # To this
    def three_letter_words(words)
      words.select { %.length == 3 }
    end

!SLIDE 
# Also works with multiple args:

    @@@ ruby
    { foo: 'bar', baz: 'qux' }.each do
       puts "#{%1}: #{%2}" 
    end

!SLIDE h3centered

# Secret: you can actually do this.

### (almost)

!SLIDE bigcode

# String#to_proc

    @@@ ruby
    (1..5).map &'_ * 2' 
    
    #=> [2, 4, 6, 8, 10]


!SLIDE bigcode

# Even crazier!

    @@@ ruby
    (1..5).map &'*2' 
    
    #=> [2, 4, 6, 8, 10]

http://weblog.raganwald.com/2007/10/stringtoproc.html


!SLIDE

# Macros: metaprogramming++

!SLIDE code meta

# Remember these?
    @@@ coffeescript
    # is
    launchMissles() if launchCode is '1234'

    # isnt
    falsifyData() if result isnt 'expected'

    # in
    leaveEarly() unless client in office

!SLIDE center cantadd

# You CAN'T add those to ruby.

----------

# You COULD if it had macros.
