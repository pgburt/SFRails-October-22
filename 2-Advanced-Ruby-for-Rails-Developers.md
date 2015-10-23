Sherif Abushadi
Teacher of Ruby and Javascript at DevBootCamp
https://twitter.com/amgando

Ruby claims to make things easier for developers. But sometimes the flexibility feels like complexity.

In ruby there are 4 diff ways to reference and later execute a piece of code:
- methods
- blocks
- procs
- lambdas

Most understand methods and maybe blocks. We should ALL understand procs and lambdas.

What about dynamic methods? You can
>>>
def do_something
 #do-it
end if true
>>>

"Clever isn't necessarily good"

Paraphrase: "You need to be twice as smart while debugging, than when you're coding. If you're clever that kills you".

## Why Procs and Lambdas?
What if you could treat code as if it were data or an object?

They work very similar to clojures in javascript. Can be saved into a variable and moved around as if they were data.

Two ways to define a lambda:
>>>
do_something = ->(param1 = "default") { puts param1 }
>>>
>>>
do_something = lambda { |param1 = "default"| puts param1 }
>>>

Do you know what the idea of 'arity' is?
Arity just means the number of parameters.

"I have an arity of one" means I have just one parameter.
Lambdas return right to the point they were invoked from.

### Procs
- Don't enforce arity.
- Return to the scope in which they were defined.

## Live coding: demonstrate knowledge in public!
He convinced someone from the crowd to demonstrate knowledge in public! Offered up 2 books as a bounty.

Hilarious live sportscasting as the audience member coded out his sample.

Called it "mob programming" as a sit in for pair programming. Audience shouted suggestions. Applauded and laughed as we stumbled through a live demonstration.

Wanted to show 2 things:
- arity
- return from scope

## Bad news about learning
You'll remember there's a difference between procs and lambdas. But, you won't remember what it is.

This is a natural process. Remember, we all do this! So, look it up again, or encourage others to look it up again.

## Example
Took a look at GitLabs. Decided to do some analysis of the code base.

Found that lambdas made it easier to reason about what was happening in the code.

Also found a lot of code that was quite confusing.

## Closing

Best state of mind is being in a state of play. Empathetic play.

Remember! Methods and blocks can NOT be passed around like objects.
Procs and lambda can.

Closing thoughts:
- Embrace confusion
- Have faith in your own work.
- Keep exploring and being playful.
