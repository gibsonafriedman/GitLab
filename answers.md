# Quiz questions

This is only a "quiz" in the loosest sense that it's asking questions whose
answers will be part of your grade. Please use *any resources you want*, as
long as you list those resources (e.g. peers, websites, etc.)

## Navigating logs

1. What is the SHA for the last commit made by Prof. Xanda on the branch
xanda_0000_movie_processing?
(For this and future questions, the first 5 characters is plenty - neither
Git nor I need the whole SHA.)
c492aa

2. What is the SHA for the last commit associated with line 9 of this file?
d1d83

3. What did line 12 of this file say in commit d1d83?
I should really finish writing this.

4. What changed between commit e474c and 82045?
Gross_sort was changed to add an int() and top_five was changed from -5 to -6.

## Predicting merges

Assume at the start of each of these three questions that your
branch for switching to a top-10 list was called `top_ten`
and your branch generalizing to any number of movies was called `top_N`.
Predict the behavior of these three possible operations - you don't
have to provide a full `diff` but you should describe at a high level
what changes would happen.

These questions are supposed to be separate paths, not cumulative;
for example, you should *not* assume that the operations of 5 were run
before 6. When testing outcomes later in the lab, you should make sure to
revert back to the state of the branch before you started these questions.

5. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout test
git merge top_N
```
If I were to run this, it would change the python file in test to be the code from top_N.

6. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout top_ten
git merge test
```
If I were to run this, it would merge the changes from test into top_ten overwriting the current code.

7. What do you think would happen if you ran the following commands?
What branches would change, and how?
```
git checkout test
git rebase top_ten
git rebase top_N
```
This would overwrite the code in the test branch to include changes from top_ten and top_N but would ultimately only included changes from both meaning the code would be ruined since both branches include changes to the code.

Extra credit?
I'm not sure if this will get me extra credit but I managed to mess up my branches and used git rm to fix some of my issue.