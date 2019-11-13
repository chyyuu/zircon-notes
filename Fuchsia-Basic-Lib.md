FBL is the Fuchsia Base Library

- system/ulib/fbl, which is usable from both kernel and userspace.
- kernel/lib/fbl, which is usable only from  the kernel.

FBL provides:

- utility code
  - [basic algorithms](include/fbl/algorithm.h)
  - [atomics](include/fbl/atomic.h)
  - [alloc checking new](include/fbl/alloc_checker.h)
- allocators
  - [slab allocation](include/fbl/slab_allocator.h)
  - [slab malloc](include/fbl/slab_malloc.h)
- arrays
  - [fixed sized arrays](include/fbl/array.h)
  - [fixed sized arrays](../kernel/lib/fbl/include/fbl/inline_array.h),
    which stack allocates small arrays
- inline containers
  - [doubly linked list](include/fbl/intrusive_double_list.h)
  - [hash table](include/fbl/intrusive_hash_table.h)
  - [singly linked list](include/fbl/intrusive_single_list.h)
  - [wavl trees](include/fbl/intrusive_wavl_tree.h)
- smart pointers
  - [intrusive refcounted mixin](include/fbl/ref_counted.h)
  - [intrusive refcounting pointer](include/fbl/ref_ptr.h)
  - [unique pointer](include/fbl/unique_ptr.h)
- raii utilities
  - [auto call](include/fbl/auto_call.h) to run
    code upon leaving scope
  - [AutoLock](include/fbl/auto_lock.h)
