Mining difficulty/target is re-calculated every 2016 blocks. The nodes look at the previous 2016 blocks and see whether these took 2016*10 minutes to mine. If it took less time than that then increase diff. If it took more time than that decrease diff. Every two weeks or so.

So the diff is adjusted using the ratio of how long it took to find the blocks/ how long it should have taken.

Take the total time it took to get the 2016 blocks. Divide that by 2016. That's the average blocktime. Take that number and divide by 10. Then multiply the target by that.

The nodes use the timestamps in the block headers to figure out how long the 2016 blocks took. All nodes have the same blockchain so they all get the same difficulty.
