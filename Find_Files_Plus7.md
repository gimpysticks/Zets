---
created: 2026-01-06
---
To find files in a specific directory (like your "mid Journey" folder) based on their age, the `find` command is the perfect tool. Since your directory name contains a space, you'll need to use quotes to ensure Linux handles the path correctly.

### The Command

Run this in your terminal:

```bash
find "mid Journey" -type f -mtime +7

```

---

### Breaking Down the Syntax

| Component            | Description                                                                         |
| -------------------- | ----------------------------------------------------------------------------------- |
| `find "mid Journey"` | Tells the command where to start looking. Quotes are required because of the space. |
| `-type f`            | Restricts the search to **files** only (excluding folders).                         |
| `-mtime +7`          | Filters for files modified **more than** 7 days ago.                                |

### Common Variations

- **To delete the files automatically:**
  If you are certain you want to remove them, add the `-delete` flag:
  `find "mid Journey" -type f -mtime +7 -delete`
  _> **Note:** Always run the command without `-delete` first to verify which files will be removed._
- **To see the file details (size, date, etc.):**
  `find "mid Journey" -type f -mtime +7 -ls`
- **To search by minutes instead of days:**
  If you need more precision, use `-mmin`. For example, `-mmin +10080` is the equivalent of 7 days in minutes.

### A Note on Time Calculation

In Linux, `+7` actually means "8 or more days ago" because of how the command rounds time. If you want exactly 7 days or more (including files from exactly the 7th day), you might sometimes see users use `+6` depending on their specific needs.
