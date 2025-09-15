# Solana Events

## Twine Chain Events

### 1. MessageTransaction

Emitted after deposit/ForcedWithdraw transaction is successfully added to the queue.

```rust
pub struct MessageTransactionEvent {
    pub event: String,          // MessageTransaction
    pub nonce: u64,
    pub l1_pubkey: String,
    pub twine_address: String,
    pub l1_token: String,
    pub l2_token: String,
    pub chain_id: u64,
    pub amount: String,
    pub data: Vec<u8>, 
    pub message_type: String,
    pub slot_number: u64,
}
```

Example:
```json
{
  "amount": "1000000000",
  "chain_id": 900,
  "data": "",
  "event": "MessageTransaction",
  "l1_pubkey": "BdhpXtonNKnVKpEK7iSzZvVU1gKSWtMjUaTuQZ4rvJkS",
  "l1_token": "11111111111111111111111111111111",
  "l2_token": "0x4ed7c70F96B99c776995fB64377f0d4aB3B0e1C1",
  "message_type": "Withdraw",
  "nonce": 11,
  "slot_number": 403666786,
  "twine_address": "0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266"
}
```


### 2. BatchCommitmentAndFinalizationSuccessful

Emitted after a batch is committed and finalized in a single transaction directly.

```rust
pub struct FinalizedBatchEvent {
    pub event: String,        // BatchCommitmentAndFinalizationSuccessful
    pub batch_number: u64,
    pub messages_handled_on_twine: u64,
    pub chain_id: u64,
    pub batch_hash: [u8;32],
    pub slot_number: u64
}
```

## Tokens Gateway Events

### 1. RefundSuccessful

Emitted after a successful refund.

```rust
pub struct RefundSuccessfulEvent {
    pub event: String,          // RefundSuccessful
    pub nonce: u64,
    pub l1_receiver: String,
    pub l1_token: String,
    pub chain_id: u64,
    pub amount: u64,
    pub slot_number: u64,
}
```

### 2. ForcedWithdrawalSuccessful

Emitted after a forced withdrawal is executed successfully.

```rust
pub struct ForcedWithdrawalSuccessfulEvent {
    pub event: String,           // ForcedWithdrawalSuccessful
    pub nonce: u64,
    pub l1_receiver: String,
    pub l1_token: String,
    pub chain_id: u64,
    pub amount: u64,
    pub slot_number: u64,
}
```

### 3. L2WithdrawExecuted

Emitted after a l2 initiated withdrawal is executed successfully.

```rust
pub struct L2WithdrawExecutedEvent {
    pub event: String,           // L2WithdrawExecuted
    pub nonce: u64,
    pub l1_token: String,
    pub l2_token: String,
    pub l1_receiver: String,
    pub chain_id: u64,
    pub amount: u64,
    pub slot_number: u64,
}
```