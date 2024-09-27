
```mermaid
flowchart TD
A[Program Loads] --> B[Is it Working?]
B -- Yes --> C[Continue Operating]
B -- No --> D[Log Error]
D --> E[Send Notification]
E --> B
C --> F[End]
```
