Appdate PHP Coding Standards

Overview
-----------

- Files MUST use only `<?php` and `<?=` tags.

- Files MUST use only UTF-8 without BOM for PHP code.

- All PHP files MUST end with a single blank line.

- Code MUST use an indent of 4 spaces, and MUST NOT use tabs for indenting.

- There MUST NOT be trailing whitespace at the end of non-blank lines.

- Blank lines MAY be added to improve readability and to indicate related blocks of code.

- There MUST NOT be a hard limit on line length; the soft limit MUST be 120 characters; lines SHOULD be 80 characters or less.

```php
<?php
namespace Vendor\Package;

class ClassName
{
    public function aVeryLongMethodName(
        ClassTypeHint $arg1,
        &$arg2,
        array $arg3 = []
    ) {
        // method body
    }
}
```

- Opening braces for classes MUST go on the next line, and closing braces MUST go on the next line after the body.

- Opening braces for methods MUST go on the next line, and closing braces MUST go on the next line after the body.

- Visibility MUST be declared on all properties and methods; abstract and final MUST be declared before the visibility; static MUST be declared after the visibility.

- Control structure keywords MUST have one space after them; method and function calls MUST NOT.

- Opening braces for control structures MUST go on the same line, and closing braces MUST go on the next line after the body.

- Opening parentheses for control structures MUST NOT have a space after them, and closing parentheses for control structures MUST NOT have a space before.

```php
<?php
if ($expr1) {
    // if body
} elseif ($expr2) {
    // elseif body
} else {
    // else body;
}
```

- A `switch` structure looks like the following.

```php
<?php
switch ($expr) {
    case 0:
        echo 'First case, with a break';
        break;
    case 1:
        echo 'Second case, which falls through';
        // no break
    case 2:
    case 3:
    case 4:
        echo 'Third case, return instead of break';
        return;
    default:
        echo 'Default case';
        break;
}
```

- A `while` statement looks like the following.

```php
<?php
while ($expr) {
    // structure body
}
```

```php
<?php
do {
    // structure body;
} while ($expr);
```

- A `for` statement looks like the following.

```php
<?php
for ($i = 0; $i < 10; $i++) {
    // for body
}
```

- A `foreach` statement looks like the following.

```php
<?php
foreach ($iterable as $key => $value) {
    // foreach body
}
```

- A `try catch` block looks like the following.

```php
<?php
try {
    // try body
} catch (FirstExceptionType $e) {
    // catch body
} catch (OtherExceptionType $e) {
    // catch body
}
```

Editorconfig
-----------
Please use [EditorConfig](http://editorconfig.org/) with you editor. There are plugins
for [SublimeText](https://github.com/sindresorhus/editorconfig-sublime)
and [Vim](https://github.com/editorconfig/editorconfig-vim) as well.

- Sample `.editorconfig`
```
root = true

[*.php]

indent_style = space
indent_size = 4

charset = utf-8
end_of_line = lf
trim_trailing_whitespace = true
insert_final_newline = true
```


Based on [PHP Standard Recommendation (PSR)](https://github.com/php-fig/fig-standards)
