![xbYRPTwo9WN5Y3c9VOGLd](https://github.com/0xmoei/alignedlayer-testnet/assets/90371338/de340f64-6873-4171-b608-d7027e61eef0)

> Aligned aims to accelerate Ethereum's roadmap by making proof verification faster and cheaper, reducing costs by up to 90%
>
> Ethereum wasn't initially designed for ZK proofs, and integrating new primitives is challenging. Aligned Layer will transform Ethereum into an efficient, cost-effective platform for SNARK verification
>
> They maintain neutrality, supporting all involved in zero-knowledge technology development and research, focused on expanding Ethereum's ZK capabilities to enable a future of trustless applications using verifiable computation and Ethereum's security.


# Submit a zkProof via AligendLayer

## Install
```console
# Update packages
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install curl -y

# Download Binaries
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/install_aligned.sh | bash

source /root/.bashrc

curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/get_proof_test_files.sh | bash
```

## Submit Proof
```console
cd /root/.aligned/test_files

aligned submit \
--proving_system SP1 \
--proof ~/.aligned/test_files/sp1_fibonacci.proof \
--vm_program ~/.aligned/test_files/sp1_fibonacci-elf \
--aligned_verification_data_path ~/aligned_verification_data \
--conn wss://batcher.alignedlayer.com
```

#

> Save the output link


#

## Verify Proof
```console
aligned verify-proof-onchain \
--aligned-verification-data ~/aligned_verification_data/*.json \
--rpc https://ethereum-holesky-rpc.publicnode.com \
--chain holesky
```
![verify proof](https://github.com/5oroo5h/alignedlayer-testnet/assets/124317301/82692850-9419-4fff-96e1-374059e212b2)



> Now post your submit-proof screenshot + output link in Twitter and tag @alignedlayer + #aligned ✅
>
![x-post](https://github.com/5oroo5h/alignedlayer-testnet/assets/124317301/9412f3f5-f5a0-4b61-b2fa-e6c371f62127)

>
> Enough for now, but we will follow the future opportunities to contribute to AlignedLayer
