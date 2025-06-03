# direct-address-table

Header-only C++ implementation of a direct-address table as described in *Introduction to Algorithms, Third Edition (3rd. ed.)*. The interface is similar to that of `std::unordered_map` as specified in the C++17 Standard, with a few exceptions:

- The elements of the container *are* ordered.
- There are no node-level operations (`extract`, `merge`, certain overloads of `insert`, etc.).
- There is no bucket interface (indeed, there are no buckets).
- There is no interface to the hash function (which, for a direct-address table, is the identity function).

In fact, it is essentially a container adaptor over a pair of `std::vector`s; as such, it has closer resemblance to `std::flat_map` (specified in the C++23 standard).
