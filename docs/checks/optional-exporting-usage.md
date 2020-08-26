[BACK](../check_documentation.md)

# Optional EXPORTING Usage
## What is the Intent of the Check?
The “Optional EXPORTING Usage” check is part of the Clean Code Check Repository, and the optional parameters make the code needlessly longer.

## How does the check work?
This check searches for the usage of the optional keyword EXPORTING in the class method calls.

## How to solve the issue?
Omit the optional keyword EXPORTING.

## What to do in case of exception?
You can suppress Code Inspector findings generated by this check using the pseudo comment `"#EC OPTL_EXP`. The pseudo comment must be placed right at the end of the statement.

## Example
```abap
  class->meth1( EXPORTING param1 = 'example' ). "#EC OPTL_EXP
```

## Further Readings & Knowledge
* [ABAP Styleguides on Clean Code](https://github.com/SAP/styleguides/blob/master/clean-abap/CleanABAP.md#omit-the-optional-keyword-exporting)