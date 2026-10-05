# Auto set urgency for high impact

## Configuration

- **Table:** Incident
- **Type:** onChange
- **Field name:** Impact
- **Active:** True

## Script

```javascript
function onChange(control, oldValue, newValue, isLoading) {
    if (isLoading || newValue == '') {
        return;
    }

    if (newValue == '1') {
        g_form.setValue('urgency', '1');
        g_form.addInfoMessage('Urgency set to High for High impact incident.');
    }
}
```

## Expected Result

When Impact is changed to High, Urgency is automatically set to High and an information message is displayed.
