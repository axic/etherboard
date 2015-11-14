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
