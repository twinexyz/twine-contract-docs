# Ethereum Events

## L1 Events

#### TransactionType

```solidity
enum TransactionType {
    Deposit,
    Withdraw,
    Message
}
```

### L1MessageHandler Events

#### 1. MessageTransaction

```solidity
event MessageTransaction(
    TwineTypes.TransactionType txnType,
    uint64 nonce,
    uint64 chainId,
    uint64 blockNumber,
    address l1Token,
    address l2Token,
    address l1Address,
    address twineAddress,
    uint256 amount,
    bytes message
);
```

### TwineChain Events

#### 1. FinalizedBatch

```solidity
event FinalizedBatch(
    uint64 indexed batchNumber,
    uint64 indexed messagesHandledOnTwine,
    uint64 chainId,
    uint256 blockNumber,
    bytes32 batchHash
);
```

#### 2. RefundSuccessful

```solidity
event RefundSuccessful(
    uint64 nonce,
    string l1Address,
    string L1TokenAddress,
    uint64 ChainId,
    string amount,
    uint64 blockNumber
    );
```

#### 3. ForcedWithdrawSuccessful

```solidity
event ForcedWithdrawalSuccessful(
    uint64 nonce, 
    string l1Address,
    string L1TokenAddress,
    uint64 chainId,
    string amount,
    uint64 blockNumber
);
```

#### 4. L2WithdrawExecuted

```solidity
event L2WithdrawExecuted(
    uint64 nonce,
    string indexed l1Token,
    string l2Token,
    string indexed receiver,
    string indexed amount,
    uint256 blockNumber
);
```

## L2 Events

### L2TwineMessenger

#### 1. SentMessage

```solidity
event SentMessage(
    address indexed from,
    address l2Token,
    string to,
    string l1Token,
    uint256 amount,
    uint256 value,
    uint256 nonce,
    uint256 indexed chainId,
    uint256 blockNumber,
    uint256 gasLimit
);
```

#### 2. TransactionFailed

```solidity
event TransactionFailed(bytes reason);
```

#### 3. L1TransactionsHandled

```solidity
event L1TransactionsHandled(
    uint256 chainId,
    uint8 status,
    uint256 nonce,
    bytes transactionOutput
);
```

#### 4. ConsensusVerified

```solidity
event ConsensusVerified(bytes consensusProof);
```