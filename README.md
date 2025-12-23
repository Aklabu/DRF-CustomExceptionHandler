## Configuration

Copy the `utils/` directory into the project root and enable the custom exception handler in `settings.py`:
```python
REST_FRAMEWORK = {
    "EXCEPTION_HANDLER": "core.exceptions.custom_exception_handler",
}
```

## Why Use This?

### ✅ Simpler frontend & mobile logic
```javascript
if (response.success) {
  use(response.data);
} else {
  showError(response.message);
}
```

- One reusable response handler
- No special cases
- Fewer bugs
- Faster development

### ❌ Without a standard

- Must check HTTP status codes manually
- Inconsistent error formats (`detail`, `error`, `errors`)
- Harder debugging
- Painful refactoring
- Unstable API contracts