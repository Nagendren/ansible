**To use this role in PB.**

  create roles folder. under roles, create requirements.yml
  in requirements.yml
  - src: https://github.com/Nagendren/ansible_create_linuxdir.git(add exact role url)
    version: master (branch/tags)
    scm: git
    
  **in main.yml**
  ---
  - name: create dir
    hosts: all
    roles:
      - role: ansible_create_linuxdir
        dir_details:
          - { path: '/tmp/test', state: 'touch', mode: '0755', recurse: 'yes', owner: 'root', group: 'root' }
          - { path: '/tmp/test1' }
  **If you are not giving any input to attributes, default vaules will be set**
