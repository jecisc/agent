# My coding conventions 

## General
- Do not use abbreviations except when the abbreviation is better known that its original name (such as HTTP). I forbid the use of temporaries or argument names with only one letter
- In multi paradigm languages, I prefer to code in OOP except if say otherwise or if I participate to a project already coded an another paradigm
- Add documentation on this that are complex but do not add comments to code that is self explanatory
- I want my code to be the simplest and more readable possible except if it can create a big bottleneck in performances
- Avoid to add dependencies iff possible. If you wish to bring a new dependency ask me if I want it
- Document public API
- Do not wrap in the middle of a line before 200 character. We now have wide screens, let's use it
- If you update code, check that class comments are still up to datex
- I am personaly using fish as shell
- To know about me: I like to code in TDD if possible

## Python 
- Use tabs for indentation and not spaces
- Use type hint if possible

## Pharo
- If a pharo mcp is connected check /Users/cyril/Library/Preferences/pharo/GitRepositories/Evref-BL/MCP/templates. If this folder exists, read the files inside. In case of contradiction the priority is: AGENTS.md of the project > ~/.opencode/AGENTS.md > MCP/AGENTS.md
- Pharo usually compiles code in memory, but it persist the code on disk when commiting in files that are using the Tonel format. Since those files are generated, the structure is really standard. Make sure to follow this structure. Methods should be first the class side methods, then the instance side one. For both they are ordered alphabetically
- Tonel method bodies require the bracket style: `selector [ body ]`. Conversely, when saving methods directly in the image (e.g. via the MCP), compile them WITHOUT brackets, since Pharo stores the method source bracket-less
- In Pharo, `Symbol` answers `true` to `#isString` (Symbol is not a String subclass but overrides `isString`), so checks like `aFlagArgument isString` also match symbols
- Use #isNotNil and not #notNil. Use #isNotEmpty and not #notEmpty
- Avoid the use of #isKindOf: when possible. If you want to use it, ask me if it's ok in this context
- If you override a method, favors the use of the protocol in the superclass
- If you send multiple messages to the same receiver, prefer a cascade except for assertions in a test case
- Pharo currently uses cr for line returns when the code is inside Pharo (in Tonel files, it is the line return of the OS). Use cr instead of lf if you compile some code in Pharo
- In Pharo indexes starts at 1 and not 0 by standard
- If you need to check the code of dependencies on the project, if there is a MCP active and the code in the image, it would be better to check in the image instead of asking me permissions to check all the clones on my computer
- Class initializations should not have a super initialize call

### Testing
- assertCollection:hasSameElements: ignores multiplicity in current images (#(a a) vs #(a) passes). Add an explicit size assertion to catch duplicates
- Do not do `self assert: a == b` but `self assert: a identicalTo: b`
- Do not write tests for simple getters and setters
- When comparing if a collection is empty or not, favor #assertEmpty: and #denyEmpty:


## Don't
- Don't use emoji if it does not bring value
- Avoid premature abstractions
