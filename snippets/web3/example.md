# Read Contract With Ethers

## Scenario

使用 ethers 读取合约只读方法。

## Example

```ts
import { JsonRpcProvider, Contract } from "ethers";

const provider = new JsonRpcProvider("https://example-rpc.local");
const abi = [
  "function balanceOf(address owner) view returns (uint256)"
];

const contract = new Contract("0x0000000000000000000000000000000000000000", abi, provider);
const balance = await contract.balanceOf("0x0000000000000000000000000000000000000000");

console.log(balance.toString());
```

## Notes

- 不要在笔记中保存私钥或助记词。
- RPC 地址如果包含 token，应使用占位符。
