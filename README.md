# Infinity.RDRE
Random Digital Root Encoding

RDRE allows information to be encoded with random numbers.

1. Create an index, mapping characters to indices. (Indicies must not contain a digit zero as there is no digital root of 0 when being derived from larger numbers)
2. Generate a random number then calculate it's digital root.
3. Substitute the index digits with a random number that matches the digital root.

The process can be optimized by pre-generating a pool of random root numbers.
```
1: [3286, 4717, 9487, 6643, 3016, 2701, 7993, 4546, 4087, 7201, 5050, 3871, 1063, 7165, 7183, 3511, 6994, 4366, 9190, 5707]
2: [1775, 5456, 4277, 1469, 1028, 9389, 7805, 4799, 6284, 4808, 2738, 3953, 8237, 6158, 8948, 2882, 8705, 3629, 5159, 5861]
3: [6807, 2424, 3216, 7266, 7608, 5439, 7635, 8751, 9363, 7257, 7347, 3549, 8490, 1623, 5160, 8958, 1668, 5574, 6186, 3720]
4: [2443, 4828, 7690, 6286, 6538, 5080, 8689, 2641, 3586, 8869, 4108, 3154, 3433, 9049, 1156, 5431, 7852, 1345, 5908, 1795]
5: [2714, 9635, 5729, 1418, 9527, 9005, 1859, 3002, 6962, 9770, 6449, 9878, 9086, 4136, 7313, 1814, 3101, 4532, 4721, 6719]
6: [3921, 4083, 9888, 4983, 9681, 1077, 2400, 9609, 9600, 5811, 8529, 4524, 3327, 5874, 8655, 2202, 3687, 5082, 1680, 5838]
7: [3211, 6559, 1150, 2707, 7981, 9853, 8962, 4750, 9484, 8206, 1573, 6631, 4705, 2572, 9340, 2824, 7504, 6163, 6622, 7864]
8: [8576, 4940, 7739, 4067, 7829, 7676, 8243, 7469, 4940, 8936, 7910, 4742, 4130, 2123, 9647, 8081, 7199, 8594, 3032, 9548]
9: [5373, 2673, 6723, 8712, 3366, 6831, 2169, 8496, 3699, 3402, 5742, 8793, 6624, 3042, 1143, 6138, 2034, 7893, 4320, 9468]
```

-Since the information is always the same, one can generate a stream of random noise that can be decoded.

-Noise can be added to multimedia in lossy streams and retried by accounting for threshold values.

-One could also implement a network socket with this encoding.
     -In my implementation, Infinity.RDRS (RDR-Stream) will maintain a realtime stream for communication.
