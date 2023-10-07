# A Kernel Seedling
An introduction to kernel building. This basic module outputs the number of running processes

## Building
```shell
    #Command to build kernel module: 
    make 
    #insert/load the kernel module 
    sudo insmod proc_count.ko
```
  

## Running
```shell
    #Command for running binary, should output processes running: 
    cat /proc/count
```
This should output processes running on system

## Cleaning Up
```shell
    #Command for removing previous build information
    make clean

    #If error inserting new module after above command + make, run: 
    sudo rmmod proc_count.ko
```

## Testing
```python
python -m unittest
```
Outputs that it ran 3 tests, either fail or say Ok

```shell
#get info about kernel release, name and version
uname -r -s -v
```
Linux 5.14.8-arch1-1 #1 SMP PREEMPT Sept 2021 (more info printed with above command but omitted)
