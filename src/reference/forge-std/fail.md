## `fail`

### Signature

```solidity
function fail(string memory err) internal virtual;
```

### Description

Provides a clean and readable way to fail tests if a certain branch or execution point is hit.

### Examples

```solidity
function test() external {
    for(uint256 place; place < 10; ++i){
        if(game.leaderboard(place) == address(this)) return;
    }
    fail("Not in the top 10.");
}
```