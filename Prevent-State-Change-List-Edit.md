# Prevent state change via list edit

## Configuration

- **Table:** Incident
- **Type:** onCellEdit
- **Field name:** State
- **Active:** True

## Script

```javascript
function onCellEdit(sysIDs, table, oldValues, newValue, callback) {
    alert('State cannot be updated using list editing. Please open the Incident.');
    callback(false);
}
```

## Expected Result

When a user attempts to change State directly from the Incident list, an alert is displayed and the change is blocked.

State changes made from the Incident form are allowed.
