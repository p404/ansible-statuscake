## Ansible-statuscake

This ansible module setups a test on statuscake API. 

### Requirements

Ansible 2.1

### Installation

Just copy the **library/status_cake_test.py** in your playbook folder

### Example usage:

    - hosts: localhost
      vars_files:
        - "dict_example.yml"

      tasks:
        - name: Create status cake test
          status_cake_test:
            username: "example_user"
            api_key: "som3thing1se3cret"
            name: "{{ item.value.url }}"
            url: "{{ item.value.url }}"
            test_tags: "something"
            test_type: "HTTP"
            check_rate: 300
          with_dict: "{{ example }}"


### TODO
* Role for Ansible galaxy
* Edge cases