# MANTRA Chain audit details
- Total Prize Pool: $60,000 in USDC
  - HM awards: $47,800 in USDC
  - QA awards: $2,000 in USDC
  - Judge awards: $5,800 in USDC
  - Validator awards: $3,900 in USDC
  - Scout awards: $500 in USDC
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts November 27, 2024 20:00 UTC
- Ends January 6, 2025 20:00 UTC

**Note re: risk level upgrades/downgrades**

Two important notes about judging phase risk adjustments: 
- High- or Medium-risk submissions downgraded to Low-risk (QA)) will be ineligible for awards.
- Upgrading a Low-risk finding from a QA report to a Medium- or High-risk finding is not supported.

As such, wardens are encouraged to select the appropriate risk level carefully during the submission phase.

## Publicly Known Issues

_Note for C4 wardens: Anything included in this `Publicly Known Issues` section is considered a publicly known issue and is ineligible for awards._

Issues directly related to cosmos-sdk, IBC, cosmwasm and their dependencies (comet-bft) will not be within the scope of this audit. Basically if it is a issue affecting all cosmos chains of the same versions then it should be out of scope.

However, if the issue arise from the custom code we made on our cosmos-sdk, or if the issues are directly affecting behavior of our custom modules, or if our custom modules are causing issues in the base cosmos modules (includes cosmwasm and IBC) then they should be included in the scope.

# Overview

Mantrachain is a global real-world assets platform built on blockchain technology. It leverages advanced blockchain features to facilitate the tokenization and trading of real-world assets.

Features:

- Real-world asset tokenization
- Advanced blockchain technology integration
- Multi-token support for transaction fees
- Custom fee market implementation
- Cosmos SDK-based architecture

## Links

- **Previous audits:**  Ottersec (report isn't public)
- **Documentation:** https://github.com/MANTRA-Chain/mantrachain/tree/v1.0.2
- **Website:** https://www.mantrachain.io/
- **X:** https://twitter.com/MANTRA_Chain

---


# Scope

*See [scope.txt](https://github.com/code-423n4/2024-11-mantra/blob/main/scope.txt)*

File                                                                  |      code
----------------------------------------------------------------------|----------
api/osmosis/tokenfactory/v1beta1/tx.pulsar.go                         |      6442
x/tokenfactory/types/tx.pb.go                                         |      3431
api/osmosis/tokenfactory/v1beta1/query.pulsar.go                      |      3145
api/mantrachain/xfeemarket/v1/tx.pulsar.go                            |      2334
x/tokenfactory/types/query.pb.go                                      |      1677
x/xfeemarket/types/tx.pb.go                                           |      1304
api/osmosis/tokenfactory/v1beta1/genesis.pulsar.go                    |      1132
api/mantrachain/xfeemarket/v1/genesis.pulsar.go                       |      1028
app/app.go                                                            |       960
x/xfeemarket/post/mocks/mock_bank_keeper.go                           |       920
api/mantrachain/tax/v1/tx.pulsar.go                                   |       883
api/mantrachain/xfeemarket/v1/query.pulsar.go                         |       760
api/mantrachain/tax/v1/query.pulsar.go                                |       754
x/xfeemarket/post/fee_test.go                                         |       682
x/tokenfactory/types/genesis.pb.go                                    |       662
api/osmosis/tokenfactory/v1beta1/params.pulsar.go                     |       654
api/osmosis/tokenfactory/params.pulsar.go                             |       649
api/mantrachain/tax/v1/params.pulsar.go                               |       593
x/tax/types/tx.pb.go                                                  |       581
x/xfeemarket/types/genesis.pb.go                                      |       575
api/osmosis/tokenfactory/module/v1/module.pulsar.go                   |       568
x/xfeemarket/types/query.pb.go                                        |       483
x/tax/types/query.pb.go                                               |       481
cmd/mantrachaind/cmd/testnet.go                                       |       471
api/mantrachain/tax/v1/genesis.pulsar.go                              |       458
api/osmosis/tokenfactory/v1beta1/authorityMetadata.pulsar.go          |       446
api/mantrachain/xfeemarket/module/v1/module.pulsar.go                 |       445
api/mantrachain/tax/module/v1/module.pulsar.go                        |       442
x/tax/types/params.pb.go                                              |       426
x/tokenfactory/types/v1beta1/params.pb.go                             |       403
x/tokenfactory/types/params.pb.go                                     |       401
x/tokenfactory/types/query.pb.gw.go                                   |       376
api/mantrachain/xfeemarket/v1/params.pulsar.go                        |       369
api/osmosis/tokenfactory/v1beta1/tx_grpc.pb.go                        |       329
x/tokenfactory/types/authorityMetadata.pb.go                          |       321
app/test_helpers.go                                                   |       308
x/xfeemarket/post/suite/suite.go                                      |       302
x/tax/types/genesis.pb.go                                             |       296
x/xfeemarket/types/params.pb.go                                       |       264
x/tokenfactory/types/msgs.go                                          |       251
x/tokenfactory/client/cli/tx.go                                       |       224
x/tokenfactory/keeper/msg_server.go                                   |       216
api/osmosis/tokenfactory/v1beta1/query_grpc.pb.go                     |       185
app/export.go                                                         |       176
cmd/mantrachaind/cmd/commands.go                                      |       171
x/tax/module/genesis_test.go                                          |       169
x/xfeemarket/post/mocks/mock_feemarket_keeper.go                      |       154
api/mantrachain/xfeemarket/v1/tx_grpc.pb.go                           |       149
x/xfeemarket/module/module.go                                         |       149
x/tokenfactory/module.go                                              |       145
x/tax/module/module.go                                                |       143
x/xfeemarket/post/fee.go                                              |       141
tests/connect/connect_integration_test.go                             |       128
x/tokenfactory/client/cli/query.go                                    |       126
x/tokenfactory/keeper/before_send.go                                  |       108
app/oracle.go                                                         |       107
x/tax/types/query.pb.gw.go                                            |       107
x/xfeemarket/types/query.pb.gw.go                                     |       107
app/queries/queries.go                                                |        99
x/tax/types/genesis_test.go                                           |        93
x/tax/keeper/msg_update_params_test.go                                |        87
app/ante.go                                                           |        85
cmd/mantrachaind/cmd/root.go                                          |        85
x/tokenfactory/keeper/createdenom.go                                  |        82
x/tokenfactory/keeper/bankactions.go                                  |        81
x/tokenfactory/types/params.go                                        |        79
x/xfeemarket/module/simulation.go                                     |        79
api/mantrachain/tax/v1/query_grpc.pb.go                               |        77
api/mantrachain/tax/v1/tx_grpc.pb.go                                  |        77
api/mantrachain/xfeemarket/v1/query_grpc.pb.go                        |        77
x/tax/keeper/keeper.go                                                |        75
x/tax/types/params.go                                                 |        74
app/genesis.go                                                        |        66
x/tokenfactory/keeper/keeper.go                                       |        66
x/tokenfactory/keeper/genesis.go                                      |        59
x/xfeemarket/keeper/msg_update_params_test.go                         |        57
x/xfeemarket/keeper/keeper.go                                         |        52
testutil/nullify/nullify.go                                           |        49
app/params/config.go                                                  |        46
testutil/keeper/tax.go                                                |        46
x/xfeemarket/module/genesis.go                                        |        46
testutil/keeper/xfeemarket.go                                         |        45
x/tokenfactory/types/denoms.go                                        |        45
x/tokenfactory/types/genesis.go                                       |        44
x/xfeemarket/keeper/msg_server_fee_denom.go                           |        44
x/tax/keeper/msg_update_params.go                                     |        43
x/tax/module/autocli.go                                               |        42
x/xfeemarket/module/autocli.go                                        |        41
cmd/mantrachaind/cmd/config.go                                        |        38
x/tax/types/msg_update_params.go                                      |        38
app/params/weights.go                                                 |        37
x/tax/module/simulation.go                                            |        36
x/tokenfactory/keeper/admins.go                                       |        36
x/tokenfactory/types/codec.go                                         |        36
app/params/proto.go                                                   |        35
x/xfeemarket/types/genesis_test.go                                    |        35
x/tokenfactory/keeper/grpc_query.go                                   |        33
x/tokenfactory/types/keys.go                                          |        32
app/test_support.go                                                   |        31
x/tokenfactory/types/expected_keepers.go                              |        30
x/xfeemarket/keeper/resolver.go                                       |        29
x/tokenfactory/types/tx.go                                            |        28
testutil/network/network.go                                           |        27
x/tax/module/abci.go                                                  |        27
x/xfeemarket/types/message_upsert_fee_denom.go                        |        27
app/post_handler.go                                                   |        26
x/tokenfactory/keeper/params.go                                       |        24
app/encoding.go                                                       |        23
x/tax/keeper/query_params.go                                          |        23
x/xfeemarket/types/genesis.go                                         |        23
x/tokenfactory/keeper/creators.go                                     |        22
x/xfeemarket/keeper/query_params.go                                   |        22
x/xfeemarket/module/genesis_test.go                                   |        22
x/xfeemarket/simulation/remove_fee_denom.go                           |        22
x/xfeemarket/simulation/upsert_fee_denom.go                           |        22
x/tokenfactory/types/before_send.go                                   |        20
x/tokenfactory/types/errors.go                                        |        19
x/xfeemarket/keeper/msg_update_params.go                              |        19
x/tax/module/genesis.go                                               |        18
x/xfeemarket/post/expected_keepers.go                                 |        18
x/xfeemarket/types/codec.go                                           |        18
x/xfeemarket/types/keys.go                                            |        18
x/tax/keeper/query_params_test.go                                     |        17
x/xfeemarket/keeper/query_params_test.go                              |        17
x/xfeemarket/types/default_resolver.go                                |        17
x/xfeemarket/types/message_remove_fee_denom.go                        |        17
cmd/mantrachaind/main.go                                              |        16
x/xfeemarket/types/expected_keepers.go                                |        16
app/wasm.go                                                           |        15
x/tokenfactory/types/events.go                                        |        15
x/tokenfactory/types/authorityMetadata.go                             |        13
app/params/encoding.go                                                |        12
x/tax/types/codec.go                                                  |        12
x/tax/types/expected_keepers.go                                       |        12
x/xfeemarket/simulation/helpers.go                                    |        12
x/tax/keeper/msg_server.go                                            |        11
x/tax/keeper/query.go                                                 |        11
x/tax/types/keys.go                                                   |        11
x/xfeemarket/keeper/msg_server.go                                     |        11
x/xfeemarket/keeper/query.go                                          |        11
app/proposals_whitelisting.go                                         |        10
testutil/sample/sample.go                                             |        10
tools/tools.go                                                        |        10
x/tax/types/genesis.go                                                |        10
x/xfeemarket/types/params.go                                          |        10
client/docs/statik/statik.go                                          |         8
x/tax/types/errors.go                                                 |         8
x/xfeemarket/types/errors.go                                          |         7
x/tax/types/events.go                                                 |         5
x/tokenfactory/types/constants.go                                     |         3
scripts/ci-goreleaser/goreleaser.go                                   |         2
app/params/doc.go                                                     |         1
client/docs/statik/init.go                                            |         1
x/tax/types/types.go                                                  |         1
SUM:                                                                  |     42898

## Scoping Q &amp; A

### General questions

| Question                                | Answer                       |
| --------------------------------------- | ---------------------------- |
| ERC20 used by the protocol              |      N/A  |
| ERC721 used  by the protocol            |      N/A        |
| ERC777 used by the protocol             |      N/A         |
| ERC1155 used by the protocol            |      N/A        |
| Chains the protocol will be deployed on | MANTRA Chain  |

### External integrations (e.g., Uniswap) behavior in scope:


| Question                                                  | Answer |
| --------------------------------------------------------- | ------ |
| Enabling/disabling fees (e.g. Blur disables/enables fees) | No   |
| Pausability (e.g. Uniswap pool gets paused)               |  No   |
| Upgradeability (e.g. Uniswap gets upgraded)               |   No  |


### EIP compliance checklist
N/A

# Additional context

## Main invariants

Tokenfactory
- The user that created a token is the token admin of that token
- Only token admin can force transfer and mint tokens


## Attack ideas (where to focus for bugs)
We have a custom tokenfactory module. We are concerned to see if this module can be exploited to have unintended behavior such as:
- minting by users not the token admin
- force transfer of tokens not done by token admin


## All trusted roles in the protocol

Mostly permissionless. 

Some functionalities are only invoked by governance through proposals and voting.


## Describe any novel or unique curve logic or mathematical models implemented in the contracts:

N/A


## Running tests

```bash
git clone --recurse https://github.com/code-423n4/2024-11-mantra.git 
cd 2024-11-mantra
go mod tidy
make install
make test
```

## Miscellaneous
Employees of MANTRA and employees' family members are ineligible to participate in this audit.

Code4rena's rules cannot be overridden by the contents of this README. In case of doubt, please check with C4 staff.



