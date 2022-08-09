# ERC721H

Gas optimized version of [ERC721A](https://github.com/chiru-labs/ERC721a) in
Huff.

## Naming Convention
- prefix all macros / constants / labels with `{FileName}__` e.g. `ERC721H__MY_MACRO`
- exceptions to above rule
  - prefix storage slot constants with `{FileName}_SLOT__`
  - name the constructor and selector switch `{FileName}_CONSTRUCTOR` / `{FileName}_SELECTOR_SWITCH` respectively
  - function signature constants do not require a prefix
- prefix macros / labels / constants that are only meant for internal use (quasi
  private) with a double underscore e.g. `__ERC721H__selectorSwitchEnd`
- use camel case for labels / custom function signatures
- use snake case for macros / constants

## Using ERC721H
### Using ERC721H - Security Considerations
- Excessively large, arbitrary `ERC721H__START_TOKEN_ID` values may lead to
  owner data storage slots colliding with other variables, leading to a suite of
  bugs / vulnerabilities
