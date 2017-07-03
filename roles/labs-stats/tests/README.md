#UPDATE DATABASE ON LABS DEMO RUNS

An ansible role that updates the database after each demo run to log statistics. If MongoDB is not installed on `dbserver` host, this role will also attempt to install it.

---
##Testing

run the test ```ansible-playbook -i inventory test_labs_stats.yml --ask-become-pass```

###Test Notes: 

* This requires that you have sudo privillege to install MongoDB on the host. If installation not needed simply comment out `become: yes` on the playbook