# large-hash-map

- ***JDK 8*** is JDK HashMap is the oldest hash map implementation.

- ***FastUtil*** is extends the Java™ Collections Framework by providing type-specific maps, sets, lists and queues with a small memory footprint and fast access and insertion.

- ***Goldman Sachs Collections*** is a collections framework for Java.

- ***HPPC*** provides array lists, array dequeues, hash sets and hash maps for all primitive types. HPPC provides normal hash maps for primitive keys and both normal and identity hash maps for object keys.

- ***Koloboke (HFTC)*** is a family of projects around collections in Java, currently provides hash maps and hash sets for all primitive/object combinations.

- ***Trove*** provides the list, stack, queue, hash set and map implementations for all primitive/object combinations.

|JDK 8|FastUtil|Goldman Sachs Collections|HPPC|Koloboke|Trove|
|---|---|---|---|---|--- |
|Maps are pretty good for Object-Object maps provided that you can tolerate the extra memory consumption and you will call HashMap constructor with required capacity = actual_capacity / fill_factor + 1 to avoid rehashing.|Consistently fast. It may become even faster if it would introduce any other storage structures except 2 arrays for keys and values.|Implementation is good enough, but is slower than FastUtil and Koloboke.|HPPC is too slow due to an extra underlying array (for cell states).|Is getting second in many tests, but it still outperforms FastUtil in int-int tests. |suffers from using mod operation for array index calculations|
