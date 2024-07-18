# Hydra Team Config

You can maintain a bash script like

```
./hydra/result/bin/hydra-node \
  --hydra-signing-key dan-hydra.sk \
  --node-id Dan \
  --port 5005 \
  --api-host 0.0.0.0 \
  --host 0.0.0.0 \
  --cardano-signing-key dan-node.sk \
  --ledger-protocol-parameters data/protocol-parameters.json \
  --testnet-magic 2 \
  --node-socket mainnet/node.sock \
  --persistence-dir ~/mainnet/persistence \
  --hydra-scripts-tx-id $(cat data/hydra-scripts-tx-id) \
  --start-chain-from $(cat data/start-chain-from) \
  --peer $(cat data/parties/arnaud.peer) \
  --hydra-verification-key data/parties/arnaud.hydra.vk \
  --cardano-verification-key data/parties/arnaud.cardano.vk \
  --peer $(cat data/parties/franco.peer)  \
  --hydra-verification-key data/parties/franco.hydra.vk \
  --cardano-verification-key data/parties/franco.cardano.vk \
  --peer $(cat data/parties/sasha.peer)  \
  --hydra-verification-key data/parties/sasha.hydra.vk \
  --cardano-verification-key data/parties/sasha.cardano.vk \
  --peer $(cat data/parties/sebastian.peer) \
  --hydra-verification-key data/parties/sebastian.hydra.vk \
  --cardano-verification-key data/parties/sebastian.cardano.vk \
    | tee -i hydra.log
```
