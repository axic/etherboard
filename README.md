# etherboard

A contract inspired by [Etherboard.io](http://etherboard.io/), combining a Ponzi-scheme with the MillionDollarHomepage.com.

This is of educational purpose, to think about how such a "scheme" can be written. It is based on the public ABI the Etherboard author has published and doesn't account for other internal features.

The price rules ([as explained here](http://etherboard.io/info)) are set out as follows:
- You can buy any unowned pixel for 5 finney or more.
- You can buy an already owned pixel for 110% or more than the price the current owner paid.
- If someone buys your pixel, you get sent 99% of the price they paid for it.
- You can change a pixel you own for 1% of its value.

NOTE: I didn't actually run this on the real network, but it compiles and looks kind of OK

Pull requests and improvements are welcome.

Also check out the [initial announcement on Reddit](https://www.reddit.com/r/ethereum/comments/3rzyp6/etherboard_an_image_powered_by_the_blockchain/).

## Optimisation

Note also that there were no attempts made to make this code optimal on execution and storage costs. After all it is for educational reasons.

Perhaps a possible way to make this more optimal is by using the below layout:

```js
mapping (uint => address) owners;
mapping (uint => uint) colors;
mapping (uint => uint) prices;

# Get the address of the pixel
# x means the columns, y means the rows
function getPos(uint x, uint y) internal returns (uint) {
    return y*1000+x;
}
```

The key for the mapping is the position given by *getPos*.

## Update

The original author has since published [the source code](http://etherboard.io/contract), but at the same time also changed some of the public API and the price calculation rules.
