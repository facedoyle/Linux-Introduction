# Linux Introduction – File Permissions Project

## Overview
This project demonstrates the management of file and directory permissions in Linux. The activity was completed as part of the Google Cybersecurity Professional Certificate. The goal was to audit file permissions, identify insecure settings, and apply corrections to align with organizational policy.

## Objectives
- Check existing file and directory permissions with `ls -la`  
- Interpret the Linux 10-character permission string  
- Identify files violating security policy  
- Update permissions using `chmod` in UGO format  
- Restrict access to hidden files and directories  

## Key Commands Used
```bash
ls -la
chmod o-w project_k.txt
chmod u=r,g=r,o= .project_x.txt
chmod u=rwx,g=,o= drafts
