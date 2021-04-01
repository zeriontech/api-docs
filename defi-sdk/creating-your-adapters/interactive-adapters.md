# Interactive adapters

## Create an interactive adapter

{% hint style="info" %}
The current version of code for interactive adapters is placed in [`interactive-updates`](https://github.com/zeriontech/defi-sdk/tree/interactive-updates) branch.
{% endhint %}

To create new token adapter, one has to implement [**InteractiveAdapter**](https://github.com/zeriontech/defi-sdk/blob/interactive-updates/contracts/interactiveAdapters/InteractiveAdapter.sol) interface. It inherits [**ProtocolAdapter**](https://app.gitbook.com/@evgeth/s/defi-sdk/~/drafts/-MRuKVgmu99bSeNK6G7Y/smart-contracts/adding-your-adapters/read-only-adapters/@drafts), so one has to implement it, too.

**InteractiveAdapters** should implement 2 main functions: `deposit()` and `withdraw()`.

{% hint style="info" %}
**InteractiveAdapters** should not have any storage variables used within deposit and withdraw functions. Use `internal constant` or `immutable constant`.
{% endhint %}

```bash
function deposit(TokenAmount[] calldata tokenAmounts, bytes calldata data)
		external
		payable
		override
		returns (address[] memory tokensToBeWithdrawn)
```

`tokenAmounts` — tokens that will be used in the action \(e.g. DAI in case of deposit to Compound\).

{% hint style="info" %}
Add `require()` if length of `tokenAmounts` should be fixed. Use the abbreviation of the contract name to use in `revert()`/`require()` errors \(later referred to as ABBR\_OF\_NAME\).
{% endhint %}

Usually, `tokenAmounts` are decomposed in `token` and `amount` like that:

```text
address token = tokenAmounts[0].token;
uint256 amount = getAbsoluteAmountDeposit(tokenAmounts[0]);
```

{% hint style="info" %}
Use `getAbsoluteAmountDeposit()` in `deposit()` function and `getAbsoluteAmountWithdraw()` in `withdraw()` function.
{% endhint %}

If tokens are required to be approved, use the following function:

```text
ERC20(token).safeApproveMax(APPROVE_RECEIVER, amount, ABBR_OF_NAME);
```

Get additional data \(e.g. user address or the desired derivative address\) required for the interaction from `bytes data` using `abi.decode` like that:

```text
address userAddress = abi.decode(data, (address));
```

Interact with the protocol using try-catch syntax:

```text
try
    Interface(callee).foo{ value: value }(arg1, arg2)
returns (returntype1, returntype2) {} catch Error(string memory reason) {
    // solhint-disable-previous-line no-empty-blocks
    revert(reason);
} catch {
    revert("ABBR_OF_NAME: deposit fail");
}
```

Fill in `tokensToBeWithdrawn` array. It should consist of tokens returning to the user \(e.g. cDAI in case of deposit to Compound\).

Remove names of unused arguments.

Use `npx prettier ./contracts/**/*.sol --write` to fix linter issues.

Add tests for interactions it `test/` directory, use Uniswap, Weth, and other required adapters.



