# Prevent save if Assigned To missing

## Configuration

- **Table:** Incident
- **Type:** onSubmit
- **Active:** True

## Script

```javascript
function onSubmit() {
    if (g_form.getValue('impact') == '1' &&
        g_form.getValue('assigned_to') == '') {
        g_form.showErrorBox(
            'assigned_to',
            'Assigned To is mandatory for High impact incidents.'
        );
        return false;
    }

    return true;
}
```

## Expected Result

If Impact is High and Assigned To is empty, the Incident is not saved and an error message is displayed.

If Assigned To is filled, the Incident can be submitted successfully.
