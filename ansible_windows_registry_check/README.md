**To use this role in PB.**

  create roles folder. under roles, create requirements.yml
  in requirements.yml
  - src: https://github.com/Nagendren/ansible_windows_registry_check.git
    version: master (branch/tags)
    scm: git
    
   **in main.yml**
   ---
   - hosts: all
     gather_facts: false
     roles:
       - role: ansible_windows_registry_check
