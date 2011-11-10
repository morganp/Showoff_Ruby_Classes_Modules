!SLIDE 
# Ruby #

!SLIDE
# Quick Review #



!SLIDE
#The .nil? Problem#

!SLIDE
# Gotcha 2 #
This works because of precedence.

    @@@ ruby
    if true == true and false == true
      puts "TRUE"
    else
      puts "FALSE"
    end

This will not give the answer you first expect:

    @@@ ruby
    a = true == true and false == true
    => false      ##<-- Looks Correct But
    puts a
    => true

The result of a `a == b` binds tightly to the left this allows the expected behavior of `not a == b`.
