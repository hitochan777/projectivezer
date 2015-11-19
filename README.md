# Projectivizer

Projectivization of non-projective dependency trees.
This is a bug fixed version of [dependency parse projectivization](http://www.cs.bgu.ac.il/~yoavg/software/projectivize/)

# Requirement

- python2.7(other 2.x might work but I didn't check)

# Usage:

```
   python projectivize.py CONLL_INPUT_FILE > PROJECTIVE_FILE
```

# Others:

   Note that this is lossy conversion. 
   If you actually care about the non-projective relations, 
   you should use a non-projective parser.  
   
   This will just help you maximize the accuracy of the projective links
   of you projective parser.

# How it converts:

   the algorithm uses Eisner's projective decoder, where links in the
   original tree are assigned a score of 1, and all other links a score
   of 0.  the decoder then finds the projective structure that has the
   maximum number of links from the original non-projective parse.

