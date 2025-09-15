# Tokens Gateway Error Codes

| SN | Hex  | Error                        | Message                                                         |
| -- | ---- | ---------------------------- | --------------------------------------------------------------- |
| 1  | 0x00 | InvalidToken                 | Invalid Token                                                   |
| 2  | 0x01 | InvalidAmount                | Invalid Amount                                                  |
| 3  | 0x02 | InvalidIndex                 | Invalid Length                                                  |
| 4  | 0x03 | InvalidAccount               | Invalid Account                                                 |
| 5  | 0x04 | InvalidReceiver              | Invalid Receiver                                                |
| 6  | 0x05 | InvalidL1Token               | Invalid L1 Token                                                |
| 7  | 0x06 | InvalidBatchNumber           | Invalid BatchNumber                                             |
| 8  | 0x07 | InvalidPDA                   | Invalid PDA derived                                             |
| 9  | 0x08 | InvalidInstructionData       | Invalid Instruction                                             |
| 10 | 0x09 | InvalidTransaction           | Invalid Transaction                                             |
| 11 | 0x0A | InvalidTokenAccount          | Invalid Token Account                                           |
| 12 | 0x0B | InvalidAddress               | Invalid address provided                                        |
| 13 | 0x0C | ReceiverAccountNotFound      | Receiver account not found                                      |
| 14 | 0x0D | WithdrawalAlreadyExecuted    | Withdraw is already executed                                    |
| 15 | 0x0E | InvalidTokenAddress          | Invalid Token address format                                    |
| 16 | 0x0F | SerializeFailed              | Failed to serialize the state                                   |
| 17 | 0x10 | NonceNotFound                | Nonce not found in withdrawals                                  |
| 18 | 0x11 | PublicValueDecodeFailed      | Failed to decode public value                                   |
| 19 | 0x12 | InvalidL2Token               | Invalid L2 token address format                                 |
| 20 | 0x13 | TokenNotFound                | Token mint not found in the vault.                              |
| 21 | 0x14 | RemoveFailed                 | Failed to remove the particular role                            |
| 22 | 0x15 | BatchNotCommitted            | Batch needs to be committed before finalization                 |
| 23 | 0x16 | Overflow                     | Overflow occurred while updating total deposits.                |
| 24 | 0x17 | QueueOverflow                | The deposit queue has reached its maximum capacity.             |
| 25 | 0x18 | InvalidArgument              | Invalid Argument provided for signature verification.           |
| 26 | 0x19 | Unauthorized                 | Unauthorized: Caller does not have the required role.           |
| 27 | 0x1A | TokenMappingNotFound         | Token decimal mapping not found for the specified token         |
| 28 | 0x1B | InsufficientFundsForTransfer | Insufficient funds in user's token account for transfer.        |
| 29 | 0x1C | BatchNotFinalized            | Batch needs to be finalized before finalizing withdrawal        |
| 30 | 0x1D | InsufficientFunds            | Insufficient funds in the vault for the requested withdrawal.   |
| 31 | 0x1E | PublicKeyMismatch            | The provided public key does not match the expected public key. |
| 32 | 0x1F | FailedToSerializeEvent       | Failed to serialize event.                                      |

# Twine Chain Error Codes

| SN | Hex  | Error                            | Message                                                                 |
| -- | ---- | -------------------------------- | ----------------------------------------------------------------------- |
| 1  | 0x00 | InvalidIndex                     | Invalid Index                                                           |
| 2  | 0x01 | NonceNotFound                    | Nonce not found                                                         |
| 3  | 0x02 | InvalidStateRootSequence         | State root mismatch                                                     |
| 4  | 0x03 | InvalidInstructionData           | Invalid Instruction                                                     |
| 5  | 0x04 | TwineVerificationError           | Error in verification                                                   |
| 6  | 0x05 | InvalidReceiptRoot               | Receipt root mismatch                                                   |
| 7  | 0x06 | InvalidTransactionType           | Invalid Transaction Type                                                |
| 8  | 0x07 | UninitializedAccount             | Account not initialized yet                                             |
| 9  | 0x08 | EmptyPreviousBatch               | Previous Batch Data is empty                                            |
| 10 | 0x09 | SerializeFailed                  | Failed to serialize the state                                           |
| 11 | 0x0A | PublicValueDecodeFailed          | Failed to decode public value                                           |
| 12 | 0x0B | InvalidDataLength                | Input data exceeds max length                                           |
| 13 | 0x0C | InvalidTokenAddressFormat        | Invalid Token Address Format                                            |
| 14 | 0x0D | InvalidBatchSequence             | Finalize in Serial batch order                                          |
| 15 | 0x0E | InsufficientFundsForTransfer     | Insufficient Funds for Transfer                                         |
| 16 | 0x0F | InvalidReceiverAddressFormat     | Invalid Receiver Address Format                                         |
| 17 | 0x10 | TokenMappingNotFound             | Token Decimal Mapping Not Found                                         |
| 18 | 0x11 | InvalidL2TokenAddressFormat      | Invalid L2 Token Address Format                                         |
| 19 | 0x12 | BatchNotFinalized                | Batch needs to be finalized first                                       |
| 20 | 0x13 | DepositRollingHashMismatch       | Deposit Rolling Hash is mismatched                                      |
| 21 | 0x14 | InvalidNonceGap                  | Copied Nonce must have required gap                                     |
| 22 | 0x15 | WithdrawRollingHashMismatch      | Withdraw Rolling Hash is mismatched                                     |
| 23 | 0x16 | PreviousBatchNotFinalized        | Previous Batch needs to be finalized                                    |
| 24 | 0x17 | RemoveFailed                     | Failed to remove the particular role                                    |
| 25 | 0x18 | LayerZeroRollingHashMismatch     | LayerZero Rolling Hash is mismatched                                    |
| 26 | 0x19 | EmptyBatchCommitment             | Commitment of Empty Batch not allowed                                   |
| 27 | 0x1A | InvalidBatchFinalizationSequence | Finalization should be done in sequence                                 |
| 28 | 0x1B | LastCommitedBatchHashMismatch    | Last commited batch hash did not match                                  |
| 29 | 0x1C | MessageExecutedCountError        | Cannot execute less message than before                                 |
| 30 | 0x1D | InvalidPDA                       | PDA derived does not equal PDA passed in                                |
| 31 | 0x1E | LastFinalizedBatchHashMismatch   | Last finalized batch hash did not match                                 |
| 32 | 0x1F | InvalidStartNonce                | Blocks must be comitted in sequential order                             |
| 33 | 0x20 | InvalidBlockCommitmentSequence   | Messages must be copied in sequential order                             |
| 34 | 0x21 | BatchHashMismatch                | Calculated and Provided Batch Hash did not match                        |
| 35 | 0x22 | InvalidSigner                    | The provided account did not sign the transaction.                      |
| 36 | 0x23 | Unauthorized                     | Unauthorized: Caller does not have the required role                    |
| 37 | 0x24 | BatchNotFilled                   | All batch data needs to be filled before finalization                   |
| 38 | 0x25 | InvalidBlockData                 | Provided startBlock/endBlock and the block data mismatch                |
| 39 | 0x26 | OverflowError                    | Overflow occurred while updating total deposits or withdrawals.         |
| 40 | 0x27 | WithdrawalAlreadyExecuted        | The withdrawal with the provided nonce has already been executed.       |
| 41 | 0x28 | GreaterCount                     | The transaction count is greater than transactions present in the queue |
| 42 | 0x29 | FailedToSerializeEvent           | Failed to serialize event.                                              |



