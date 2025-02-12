# Custom Inputs

When using the editor view to create test scenarios, you will notice the **downwards arrow button** next to an input field. This enables you to switch the method for inputting field data.&#x20;

![](<../.gitbook/assets/image (95).png>)

There are multiple options available:

| Input Type                   | Description                                                                                                                                                                                                                                                     |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Plain                        | This is a standard field. The value is not interpreted.                                                                                                                                                                                                         |
| Field Selection (JSON Query) | <p>Use this to access record data and record metadata when making <a href="building-tests/test-checks/">Test Checks</a>. <br><br>For the technical capabilities of JQ, refer to <a href="https://stedolan.github.io/jq/manual/#Basicfilters">this</a> link.</p> |
| Template (mustache)          | Access different properties such as [environment](environments/) and [local](building-tests/tasks/set-variable-task.md) variables through a selection modal in the UI                                                                                           |
| JavaScript                   | Create dynamic values or manipulate your data using JavaScript                                                                                                                                                                                                  |

**Quick links:**

* [Plain](custom-inputs.md#plain-input-selection)&#x20;
* [Field selection (JSON Query)](custom-inputs.md#field-selection-json-query)
* [Template (Mustache)](custom-inputs.md#template-mustache)
* [JavaScript](custom-inputs.md#javascript-input)

## Plain input selection

Using the plain input selection will not interpret the inputted data.&#x20;

You might use this input for simple test scenarios, where you want to manually define a literal value.&#x20;

![](<../.gitbook/assets/image (149).png>)

## Field Selection (JSON Query)

Use the Field Selection (JQ) option when creating [Test Checks](building-tests/test-checks/). This enables you to access record data and record metadata so you can test the data.

For example, access the record value for a consumed message, and assert the expected value.&#x20;

See [Accessing Kafka message data](building-tests/test-checks/accessing-kafka-message-data/) for more information.

![](<../.gitbook/assets/image (57).png>)

Below shows a **more powerful JQ example**. It utilizes a Boolean check to evaluate the length of a value within a defined range.

![](<../.gitbook/assets/image (3).png>)

## Template (mustache)&#x20;

This input method allows you to select from variables (environment or local) using a modal within the UI.&#x20;

When Template is used, click inside the input to show a **'+'** button.

![](<../.gitbook/assets/image (94).png>)

This will render a modal that presents any configured variables for selection.&#x20;

![](<../.gitbook/assets/image (29).png>)

When using JSON format to define data, it's possible to use the mustache selection to populate the key or value for a specific node.

![](<../.gitbook/assets/image (44).png>)

## JavaScript input

This input type will enable you to execute a JavaScript snippet. You might use this to create a dynamic value, or to manipulate some data.

For example, you could use a JavaScript snippet to compare a timestamp to the current date/time when a scenario is run.&#x20;

![](<../.gitbook/assets/image (124).png>)

Below shows another example of utilizing Javascript to evaluate if an expression is true.&#x20;

![](<../.gitbook/assets/image (167).png>)
