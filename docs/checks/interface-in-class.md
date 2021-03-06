[BACK](../check_documentation.md)

# Interface in Class Check
## What is the Intent of the Check?
The Is Interface in Class check searches for public methods without an interface.

## How does the check work?
This check counts only `DATA` and `CLASS-DATA` within a global or local, `CLASS DEFINITION` or `INTERFACE`. Inherited attributes and all constants are not counted. A structure is counted as one attribute, no matter how many attributes are in the structure.

## Which attributes can be maintained?
![Attributes](./img/interface_missing.png)

## How to solve the issue?
Make sure to implement an interface for the public methods.

## What to do in case of exception?
You can suppress Code Inspector findings generated by this check using the pseudo comment `"#EC INTF_IN_CLASS`. The pseudo comment must be placed right after the `PUBLIC SECTION` statement.

### Example
```abap
CLASS class_name DEFINITION.
  PUBLIC SECTION. "#EC INTF_IN_CLASS
ENDCLASS.
```

## Further Readings & Knowledge
* [ABAP Styleguides on Clean Code](https://github.com/SAP/styleguides/blob/master/clean-abap/CleanABAP.md#public-instance-methods-should-be-part-of-an-interface)
