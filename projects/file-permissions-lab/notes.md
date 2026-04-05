## File Permissions Lab

### Objective
Understand and control file access permissions in Linux to secure sensitive data.

### Steps Performed
1. Created a file containing sensitive data
2. Checked default file permissions
3. Identified that the file was readable by others
4. Restricted access using chmod 600
5. Created a secondary user to simulate an attacker
6. Attempted to access the file from another user account

### Commands Used
- touch
- echo
- ls -l
- chmod
- adduser
- su
- cat

### Key Concepts Learned
- File ownership and permissions
- Read, write, execute access levels
- Principle of least privilege
- User isolation

### Outcome
Successfully restricted access to a sensitive file and prevented unauthorized user access.

### Security Insight
Improper file permissions can expose sensitive data. Restricting access ensures only authorized users can read or modify files.
