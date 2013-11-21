tableOperations
=======================
Easily create tables with select-able rows, and operations that can be performed on the selected rows.

**Use**
To create an operation table, simply call tableOperations on the table:
<code>$('#myTable').tableOperatons(options);</code>

**Options**
```javascript
  var options = {
    defaultSelect: 'Select',
    selectClass: 'form-control',
    buttonClass: 'btn btn-default',
    formClass: 'form-inline',
    buttonText: 'Go',
    operations: {
      delete: {
        label: "Delete Selected",
        callback: function($selected) {
          $selected.each(function(index, item) {
            //Operate on item
          });
        }
      },
      save: {
        label: "Save Selected",
        callback: function($selected) {
          $selected.each(function(index, item) {
            //Operate on item
          });
        }
      },
    }
  }
```

The operations object defines the operations that will be added to the select list above the table. Upon the submition of the operation form, the selected item's callback parameter will be called with a jQuery object of the selected items passed in as the only parameter.
