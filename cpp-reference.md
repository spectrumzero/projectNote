## std::priority_queue

*EXAMPLE *
```cpp
priority_queue<int, vector<int>, greater<int>> minHeap;
```  

|                                                                                                                                                                                                                                                                                                 |     |     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --- | --- |
| template<  <br><br>    class T,  <br>    class Container = [std::vector](http://en.cppreference.com/w/cpp/container/vector)<T>,  <br>    class Compare = [std::less](http://en.cppreference.com/w/cpp/utility/functional/less)<typename Container::value_type>  <br><br>> class priority_queue; |     |     |
|                                                                                                                                                                                                                                                                                                 |     |     |

|           |     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| --------- | --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| T         | -   | The type of the stored elements. The program is ill-formed if `T` is not the same type as `Container::value_type`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Container | -   | The type of the underlying container to use to store the elements. The container must satisfy the requirements of [SequenceContainer](https://en.cppreference.com/w/cpp/named_req/SequenceContainer "cpp/named req/SequenceContainer"), and its iterators must satisfy the requirements of [LegacyRandomAccessIterator](https://en.cppreference.com/w/cpp/named_req/RandomAccessIterator "cpp/named req/RandomAccessIterator"). Additionally, it must provide the following functions with the [usual semantics](https://en.cppreference.com/w/cpp/named_req/SequenceContainer#Optional_operations "cpp/named req/SequenceContainer"):<br><br>- front(), e.g., [std::vector::front()](https://en.cppreference.com/w/cpp/container/vector/front "cpp/container/vector/front"),<br>- push_back(), e.g., [std::deque::push_back()](https://en.cppreference.com/w/cpp/container/deque/push_back "cpp/container/deque/push back"),<br>- pop_back(), e.g., [std::vector::pop_back()](https://en.cppreference.com/w/cpp/container/vector/pop_back "cpp/container/vector/pop back").<br><br>The standard containers [std::vector](https://en.cppreference.com/w/cpp/container/vector "cpp/container/vector") (including [`std::vector<bool>`](https://en.cppreference.com/w/cpp/container/vector_bool "cpp/container/vector bool")) and [std::deque](https://en.cppreference.com/w/cpp/container/deque "cpp/container/deque") satisfy these requirements. |
| Compare   | -   | A [Compare](https://en.cppreference.com/w/cpp/named_req/Compare "cpp/named req/Compare") type providing a strict weak ordering.<br><br>Note that the [Compare](https://en.cppreference.com/w/cpp/named_req/Compare "cpp/named req/Compare") parameter is defined such that it returns true if its first argument comes _before_ its second argument in a weak ordering. But because the priority queue outputs largest elements first, the elements that "come before" are actually output last. That is, the front of the queue contains the "last" element according to the weak ordering imposed by [Compare](https://en.cppreference.com/w/cpp/named_req/Compare "cpp/named req/Compare").                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

[ORIGIN](https://en.cppreference.com/w/cpp/container/priority_queue)