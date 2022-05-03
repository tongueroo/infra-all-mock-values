# Terraspace Example Project

Example terraspace project to test `terraspace all` and mock values in tfvars file.

Related: https://community.boltops.com/t/terraspace-plan-all-gets-stuck-when-mock-values-are-used-in-tfvars/874

## Deploy

    terraspace all up

## Debugging Session Example

    $ terraspace all up -y
    Running:
        terraspace up b1 # batch 1
        terraspace up a1 # batch 2
    Batch Run 1:
    Running: terraspace up b1 Logs: log/up/b1.log
    terraspace up b1:  Changes to Outputs:
    terraspace up b1:  Apply complete! Resources: 1 added, 0 changed, 0 destroyed.
    Batch Run 2:
    Running: terraspace up a1 Logs: log/up/a1.log
    terraspace up a1:  Changes to Outputs:
    terraspace up a1:  Apply complete! Resources: 1 added, 0 changed, 0 destroyed.
    Time took: 5s

    $ terraspace all down -y
    Running:
        terraspace down a1 # batch 1
        terraspace down b1 # batch 2
    Batch Run 1:
    Running: terraspace down a1 Logs: log/down/a1.log
    terraspace down a1:  Changes to Outputs:
    terraspace down a1:  Changes to Outputs:
    terraspace down a1:  Destroy complete! Resources: 1 destroyed.
    Batch Run 2:
    Running: terraspace down b1 Logs: log/down/b1.log
    terraspace down b1:  Changes to Outputs:
    terraspace down b1:  Changes to Outputs:
    terraspace down b1:  Destroy complete! Resources: 1 destroyed.
    Time took: 6s

    $