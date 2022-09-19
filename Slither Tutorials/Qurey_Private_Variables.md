# How to query private variables using Slither

Let's consider this smart-contract:
[Frax Finance](https://etherscan.io/address/0x853d955aCEf822Db058eb8505911ED77F175b99e#readContract) of which we want to read the contents of this dynamic array:

    frax_pools_array

To do so, we type this in bash, after installing slither-analyzer:

```bash
slither-read-storage 0x853d955aCEf822Db058eb8505911ED77F175b99e --variable-name frax_pools_array --rpc-url $rpc_url --value

```

And this is the output you should get:

    INFO:Slither-read-storage:
    Contract 'FRAXStablecoin'
    FRAXStablecoin.frax_pools_array with type address[] is located at slot: 18
    INFO:Slither-read-storage:
    Name: frax_pools_array
    Type: address[]
    Slot: 18
    INFO:Slither-read-storage:
    Value: 25
