## How to use <Role>/files

Role specific files allow version controlled storage of files needed for a specific ansible role. 

To copy files from the files folder to the host you do not need to specify exact path from host machine as ansible always presumes you want to copy from root of files directory

`
- name: Copy example.yml
  ansible.builtin.copy:
    src: example.yml
    dest: /etc/example.yml
`
so just specifying `example.yml` works