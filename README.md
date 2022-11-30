# Installation

1. `pip install ansible_merge_vars`
2. Make sure you have Ansible 2.4+ installed.

# How It Works?

The Python script look for the suffix keyword in any file that is in the scope of the running playbook and merge all that data into a single file.

By default, it automatically removed duplicate keys. However, if you want, you can enable duplicated using `dedup`:

```
- name: Merge data
  merge_vars:
    suffix_to_merge: _suffix__to_merge
    merged_var_name: merged_file
    expected_type: 'list'
    dedup: false
```

For advanced functionality, look into the plugin's documentation: https://pypi.org/project/ansible-merge-vars/