# Convert a long and thin table to a FAT one


### Concepts

##### Imagine a firefly detection problem from the link as below
[https://github.com/thejourneyofman/FireFly](https://github.com/thejourneyofman/FireFly)
##### New fireflies show up on time sequence and old fireflies are gone (However in this homework, all old fireflies will be saved frame by frame in the matrix, see Pic 1.).
##### As for each frame in the video, new fireflies will be added to the list and features are updated for old ones. (In case that old fireflies are gone, their features will NOT be removed but just kept in the array, that's why the array will look long and thin).
##### Given that number of features are fixed in a small number like 10 but thousands or millions of fireflies will constantly show up on the time line, that is, the original array will be pretty a long and thin one (let’s say a diet dataset, oppositely a fat dataset).
##### The purpose 1 for this homework is to flatten the diet dataset near to a square, for an instance, a 10M rows X 10 cols array will be transformed to be a near-square matrix (See Pic 2.).
##### The purpose 2 is, each object has a unique position in the new matrix and can be identified by an index. And a good design of the index will be a bonus. Given a specific object id and a timestamp, it can return the ‘features of the object at the timeframe’ by a quick index search.
##### The purpose 3 is, given that a new frame at t(i) is added, in the logic of page 3, we only have to refer to the previous matrix at t(i-1), however the matrix size is getting larger by time series, and the time complexity should be taken into consideration.

![Concept](https://raw.githubusercontent.com/thejourneyofman/diettable/master/images/p1.png)

![Concept](https://raw.githubusercontent.com/thejourneyofman/diettable/master/images/p2.png)

### Requirements
##### Implement your algorithms in python, C++ or R Lang.
##### The function definition should be as simple as possible, like by two inputs, one is the original 2-D array and another one is a timestamp, while the only output is a 2-D matrix on that timeframe for an instance.
##### Design a data store or just refer to PyStore that can load/save each matrix by timestamp without using any database including document-oriented ones like JSON at all. But you are encouraged to leverage compression/ decompression libraries to achieve a faster access to your data store.
##### As for each transformation of a new time frame, it would only refer to the matrix of last timeframe, meanwhile the size of matrixes are getting larger with more objects will be recorded by time series. A bonus is the complexity of your algorithms and the entire function.
##### To reach the goal in a MVP manner, you can either choose to import libraries as necessary as it is that could prove more your practical coding ability or import libraries as little as it is where your algorithmetic coding skill can be highlighted. Up to you!

Enjoy this short journey!

Copyright (c) 2020 Chao (Chase) Xu