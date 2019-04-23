---
layout: video
title: "100x Faster Clone Deletion for ZFS"
date: 2019-06-08
author: Sara Hartse
email: sara.hartse@delphix.com
youtube: yQGGwhDxkdw
---
Why is deleting a clone so much slower than writing one? Does it have to be? This talk will cover how ZFS clone deletion works today and why its performance is terrible in certain situations. I will present a new algorithm which addresses this problem and speeds up clone deletion by 100x. I’ll cover the design details and performance tradeoffs of the new method.

ZFS can create and modify clones (mutable copies) of large filesystems extremely quickly. These operations are fast because ZFS employs a copy-on-write strategy, meaning that all blocks of the original filesystem are shared with the clone until a block is modified. Deleting a clone is not as fast nor as simple. It requires disentangling these block dependencies, locating the blocks that belong only to the clone and are not relied upon by the original. The current clone deletion algorithm achieves this by traversing the entire block tree, ignoring sections that are still shared.

This talk will cover an alternate method of clone deletion: keeping track of clone blocks when they are modified so that, when it’s time to delete, the clone-specific blocks are already at hand. We see a performance gain because now deletion work is proportional to the number of clone-modified blocks, not the size of the block tree.

I’ll go over the implementation details of this algorithm and the performance gains I saw. Further, I’ll discuss how I addressed scalability concerns such as bounding the size of the block-tracking data structure, managing the new performance costs incurred at write time, and determining the point of diminishing returns when we should revert to the old method.