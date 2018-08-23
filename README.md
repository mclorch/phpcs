# NocWorx PHP Coding Standard

1. Indention: always 2 spaces
- Always place opening brace on same line of block declaration
- Indent all block bodies one level (2 spaces)
- Closing brace of any block is -2 spaces from the body's indention and on its own line (exceptions for `else`, `elseif`, `do-while`, and multiline function call/declaration)
- Function calls or declarations needing multiple lines, follow indention guidelines for blocks. The opening brace for a declaration appears on the same line as the closing paranthesis.
- Line length: 79 + \n
- Comments
  1. Use doc block style comments on each files, classes, functions, methods, and class properties
  - File doc block must include our legal template
  - Class doc block must include `@package`. Include `@subpackage` only if applicable
    - Package name will correlate with the repo name (eg. "Lib" for the "nocworx/lib" repo)
    - Subpackage name will correlate with a module name in the repo (eg. "Client" for the "nocworx/core" client module)
  - Method doc block must include `@param`, `@returns`, `@throws` where applicable to the method itself (not parent). Omit where not applicable.
- Strings
  1. Use single quotes for plain strings
  - Use double quotes for including variables and function/method calls (as opposed to breaking in and out with concatenation
  - Always encapsulate variables and function/method calls in curley braces
- All text must use language string placeholders. No English (or other language) in the code.
- Always a single space around operators (including assignment operator)
- Always a single space after a keyword (if, while, etc.)
- One space after but not before a comma separator unless at the end of a line
- Arrays
  - Never use `array()` - use `[]` instead
  - Push with `[]` instead of `array_push()` (eg. `$food[] = 'banana'`)
  - If not on one line, each element must be on their own line. Follow indention guidelines for blocks.
- Naming
  - All naming
    1. Must start with a letter (with the exception of certain class properties and methods below)
    - Must only contain word characters
    - Use descriptive names (single letter names acceptable only for simple loops)
    - Avoid abbreviations
  - Functions (and class methods): always use camelCase
  - Classes: always use TitleCase
  - Non-public class properties must start with a single underscore then lowercase letter
  - Non-public class methods must start with a single underscore then lowercase letter
  - Constants: always use CAPITAL_SNAKE_CASE
  - Array keys: always use snake_case
  - Event names: colon separated scopes, kebab-case each scope name but prefer single word names
  - All others: always use snake_case
- Classes should not contain public properties. Use setters and getters.
- Ternary
  - Never nest ternary statements
  - Wrap the condition in ()
  - Must be contained on either one or three lines
  - The shorthand `?:` may be used as a substitute for the expression `empty($a) ? $a : $b` (note, `$a` must be defined)
- Every block (if, while, etc.) must be contained in braces
- Concatentation operator at the end of the line for multiline statements
- Multiline strings should be concatenated. Indent two spaces from indention of the first line.
- Use a single blank line to separate logical groupings statements. More than one consecutive blank line is prohibited.
- Parenthesis must hug contents
- Conditionals
  - Never use `else if`. Always `elseif`.
  - Always use identity checks over equality checks (=== vs. ==)
  - All conditions should be explicit and evaluate to a boolean
  - Falsey checks are not acceptable BAD: `if($s)` Unless `$x` is boolean
  - Do not assign while checking. BAD: `if (x = something()) {`
- Use paren bracket style delimiters for preg_* functions and the like `preg_match('(^\d+)', $text)`
- No trailing whitespace on any line
- Every file must end with a single new line character
- For any case not explicitly addressed here, consult [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)
