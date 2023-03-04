## Using Python to encode string

```py
import base64

data = "Python is a programming language"
data_bytes = data.encode('ascii')

base64_bytes = base64.b64encode(data_bytes)
base64_string = base64_bytes.decode('ascii')

print("Encoded Data: ", base64_string)

# Output:
Encoded Data:  UHl0aG9uIGlzIGEgcHJvZ3JhbW1pbmcgbGFuZ3VhZ2U=
```
