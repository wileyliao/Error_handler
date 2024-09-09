# Error_handler
Catch except from functions


```python
def error_handler(func):
    def wrapper(*args, **kwargs):
        try:
            return func(*args, **kwargs)
        except Exception as e:
            error_message = f'{func.__name__}: {e}'
            raise RuntimeError(error_message)
    return wrapper
```
