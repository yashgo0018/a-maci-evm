<!-- # Step 1

- 生成 zkey 文件，并且提供一次贡献。（更推荐收集公共的可信证明并生成最终的 zkey 文件）
- 导出各自的 `verification_key.json`

### 性能

    运行环境: AMD Ryzen 5 5600X 6-Core Processor

    电路配置:
      stateTreeDepth: 7
      intStateTreeDepth: 3
      voteOptionsTreeDepth: 3
      batchSize: 125

    g16s-msg.sh:
      生成时间: 1294s

    g16s-tally.sh:
      生成时间: 833s

    gen-zkey-msg.sh:
      生成时间: 269s

    gen-zkey-tally.sh:
      生成时间: 139s -->

### Step 1

Download ptau file from [here](https://github.com/iden3/snarkjs?tab=readme-ov-file#7-prepare-phase-2), and put powersOfTau28_hez_final_22.ptau file into './ptau' directory.

### Step 2

Generate zkey:

```
$ ./shell/s2/g16s.sh msg

$ ./shell/s2/gen-zkey.sh msg
```

Run the above scripts for four circuits (msg/tally/deactivate/addKey) separately.
