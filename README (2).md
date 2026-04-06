# Project Files

This folder contains a small support-ticket dataset and companion documentation.

## Files

- `paste.txt`  
  Tab-separated support ticket dataset (see `README_paste.md`).

- `paste_dashboard.html`  
  Generated static dashboard (see `README_paste_dashboard.md`).

## Quick start

```python
import pandas as pd
support_df = pd.read_csv('paste.txt', sep='	')
print(support_df.head())
```

