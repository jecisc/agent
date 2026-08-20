# My coding conventions 

## General
- Do not use abbreviations except when the abbreviation is better known that its original name (such as HTTP). I forbid the use of temporaries or argument names with only one letter
- In multi paradigm languages, I prefer to code in OOP except if say otherwise or if I participate to a project already coded an another paradigm
- Add documentation on this that are complex but do not add comments to code that is self explanatory
- I want my code to be the simplest and more readable possible except if it can create a big bottleneck in performances
- Avoid to add dependencies iff possible. If you wish to bring a new dependency ask me if I want it
- Document public API
- Do not wrap in the middle of a line before 200 character. We now have wide screens, let's use it


## Python 
- Use tabs for indentation and not spaces
- Use type hint if possible

## Pharo
- Pharo usually compiles code in memory, but it persist the code on disk when commiting in files that are using the Tonel format. Since those files are generated, the structure is really standard. Make sure to follow this structure. Methods should be first the class side methods, then the instance side one. For both they are ordered alphabetically
- Use #isNotNil and not #notNil. Use #isNotEmpty and not #notEmpty

## Don't
- Don't use emoji if it does not bring value
- Avoid premature abstractions
