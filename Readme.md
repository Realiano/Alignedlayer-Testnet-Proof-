# ALIGNEDLAYER PUBLIC PROOF TASK  

![image](https://github.com/Realiano/Alignedlayer-Testnet-Proof-/assets/31314340/4ab13f14-e030-46e4-84c2-ba4e9e6e73c3)


## Getting Srtarted 

```
sudo apt update -y
sudo apt upgrade -y
```

### Install curl 
```
sudo apt-get install curl -y
```

### Download ALignedProof 
![image](https://github.com/Realiano/Alignedlayer-Testnet-Proof-/assets/31314340/0579db8f-a1ea-46dc-a32b-5589548cf502)

```
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/install_aligned.sh | bash
```

```
source /root/.bashrc
```


### Download an example SP1 proof file with it's ELF file 
![image](https://github.com/Realiano/Alignedlayer-Testnet-Proof-/assets/31314340/a5a6d803-fa4c-4247-a973-3ee02935565e)


```
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/get_proof_test_files.sh | bash
```


### Sending proof 

![image](https://github.com/Realiano/Alignedlayer-Testnet-Proof-/assets/31314340/39106cd6-7960-4a95-9c1b-acfd81d133f2)

```
rm -rf ~/aligned_verification_data/ &&
aligned submit \
--proving_system SP1 \
--proof ~/.aligned/test_files/sp1_fibonacci.proof \
--vm_program ~/.aligned/test_files/sp1_fibonacci-elf \
--aligned_verification_data_path ~/aligned_verification_data \
--conn wss://batcher.alignedlayer.com
```

use this code to get the log you will screenshot for your X post
```
aligned verify-proof-onchain \
--aligned-verification-data ~/aligned_verification_data/*.json \
--rpc https://ethereum-holesky-rpc.publicnode.com \
--chain holesky
```






