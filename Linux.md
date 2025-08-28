# File Permissions in Linux

## Project description
In this project, a security professional was responsible for managing file and directory permissions using Linux commands. Existing authorizations were reviewed, insecure settings were identified, and permissions were updated to align with organizational policy. This ensured that sensitive research files were protected from unauthorized modification or access. 

---

## Check file and directory details

### Describe the permissions string
Example: **`drwxr-xr-x`**

- **d** : Directory  
- **-** : Regular file  
- **rwx** : Owner has read, write, and execute permissions  
- **r-x** : Group has read and execute permissions  
- **r-x** : Others have read and execute permissions  

**Example violation:**  
`project_k.txt` → **`-rw-rw-rw-`**  
This means the file can be read and modified by the owner, group, and others. This violates policy because “others” should not have write access.

---

## Change file permissions
The text file `project_k.txt` was identified as having write permissions for “others” (`-rw-rw-rw-`), which is against company policy.  
The `chmod` command was used to update the permissions and align them with policy:  

```bash
chmod o-w project_k.txt
