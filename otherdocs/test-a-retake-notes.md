# Topic Test A Retake Notes

## The Why

The marks were low. Like...really low. MRU policy doesn't allow me to re-weight stuff in the course outline, so I can't just say "we'll move x weight from this exam to the next". I also am not gonna curve this, because I honestly feel it was a fair test. So that leaves me with either letting people swing, which seems devastating and cruel, or giving folks another chance. So here we are.

## The How

I've chosen 8 of the questions that seemed to give people the most trouble. You'll get a new test on Wednesday that consists of those 8 questions: I'm literally making a copy of **your** test that just has those 8 questions on it - so your marks for those questions will be there, along with your answers from last Friday.

You'll have 50 minutes to write this new test. 
> _How did I get that number? The questions you're writing make up 60% of the original test's total marks, so I reckoned I'd give you about 60% of the original test's time as well._

I'll mark this new test, bring in your marks from the other 5 questions on the original exam, and combine them to get a new score. You'll get 80% of your improvement (rounded up) added to your old score. That's probably confusing, so here's an example:

> Let's say you got a 40% on the original exam. You rewrite the exam and when your new answers are scored, the result of your combined test is now a 75%. 
> 
> In this case, you've improved your score by 35% (75% - 40%). So you'll get 80% of that improvement added to your original score. 80% of 35% is **28%**.
> 
> So your final score for Topic Test A would be 40% (your original score) + 28% (80% of your improvement) = **68%**. 

## The Questions Being Revisited

Here are some brief notes about the questions being revisited.

### Question 1 (Big O from growth functions)

From the Big O cheat sheet, one can conclude that nlogn grows faster than both n and logn. That makes sense, since nlogn has 2 parts (n and logn) that both depend on n....

### Question 3 (software team, growth functions)

Does it make sense to even **talk** about Big O when we're dealing with at most 10 items!?!?

### Question 4 (growth function from pseudocode)

Better practice up. And read the assumption.

**Also, gather like terms or you'll lose a mark.** (I didn't say that on the original test, but I **am** saying it now.) 

- ((n-4)/2) + (2n-2)*(n) + 5 ? yuck  
- n/2 - 2 + 2n^2 - 2n + 5 ? getting there...but not there yet   
- \- 3n/2 + 2n^2 + 3 ? this is ok, but  
- 2n^2 - (3/2)n + 3 ? this is best (it's in descending order of n and the coefficients are obvious)    

### Question 5 (growth function from Java)

That while loop was tricky, eh?
Also, what to do when you have if/else-if/else?...

> _Side note: for the else, I'm fine whether you count the else as 1 operation or not. In the screencasts, I did, but you don't have to._

**As with question 4, gather like terms or get penalized a bit.**

### Question 6 (talking about autogen'd equals)

A lot of this question was covered in the Implementing equals screencast. (good thing there are those notes in the video description)

If asked to explain code in English, it doesn't mean "repeat the code in English". It means "summarize at a high level what the code is doing".

### Question 9 (implement comesBefore / comesAfter)

If you implement Comparable, you must have a compareTo. The compareTo method returns an int. When that int is negative, what does that **mean**? When that int is positive, what does that **mean**?

### Question 11 (array initialization, Wat?)

What happens when you initialize arrays in a variety of ways? What are in those array "slots"? 

### Question 12 (ArrayList API)

If you're not totally familiar with terms like 

- **return type**
- **(method) signature**
- **non-static**
- **argument**, and 
- **type parameter (this is in the context of generics)** 
  
then this was a challenging question.