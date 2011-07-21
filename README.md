#About
**TinyValidation** is a jQuery plugin for simple form validation. It validates fields using built-in validators (`'notEmpty'`, `'email'`) or custom validation functions. You specify which form elements to validate through a `'data-validate'` HTML attribute, which is common-separated list of validators to run for that element.

##Example

Example markup:

    <form id="form1">
      <label for="name">Name</label>
      <input type="text" id="name" data-validate="notEmpty" />
      <label for="email">Email</label>
      <input type="text" id="email" data-validate="email, notEmpty" />
    </form>

Example JavaScript:
  
    $('#form1').tinyValidation({validateOnKeyUp: true});


##Options
The following options can be passed to `'tinyValidation'` in an optional hash:

  * `'validateOnBlur'`. Determines whether validations are run on blur events. Default: `'true'`.
  * `'validateOnKeyUp'`. Determines whether validations are run on keyUp events. Default: `'false'`.
  * `'errorClass'`. The name of the class added to form elements with invalid values. Default: `'error'`.
  * `'validClass'`. The name of the class added to form elements with valid values. Default: `'valid'`.
  * `'onError'`. Function called after a field has failed validation. The first argument passed to the function is the form element, and the second is an array of error messages (as strings). Default: `'null'`
  * `'onValid'`. Function called after a field has been validated successfully. The function will be passed the form element that was validated.
  * `'validators'`. A hash in which the keys are the names of validation functions, and the values are functions that accept an input value and return true if the validation succeeds, and false (or an error message) if the validation fails.

##License
TinyValidation is released under a 3-clause BSD license.
