
&nbsp;

***

##### C++ storage containers

* static (roughly program lifetime global namespace)
* automatic (roughly stack)
* dynamic (roughly heap)
* thread

examples:

    int q;                           // static object (global objects are static by default)

    void func()
    {
        int q;                       // automatic object

        int *p = new int;            // automatic pointer to dynamic object
        int *r = &q;                 // automatic pointer to automatic object
        static int *s = p;           // static pointer to dynamic object
        static int *s = r;           // static pointer to automatic object (bad idea)
        thread_local int **t = &s;   // thread pointer to static object 
    }

&nbsp;

***

##### automatic (aka stack)

* Allocated in RAM 
* typically stores:
  * local (auto) variables
  * function arguments 
  * return address (program counter)
* variables get deallocated when out of scope (stack unwinding - RAII)
* Faster mem allocation than heap
* Implemented with an actual stack data structure (LIFO)
* Pre-defined maximum size before program starts (e.g. default stack size for a thread spawned with pthread_create() is 2MB).
* Use case: you know how much mem you need before compile time and it's less reasonable with respect to max stack size
* Stack overflow is possible (typically from unbound recursion or large mem allocations).

##### dynamic storage (aka heap)

* Stored in computer RAM just like the stack.
* In C++, variables on the heap must be destroyed manually and never fall out of scope, data is freed with delete, delete[], or free (! old school - not true for C++11 onwards - unique_ptr/shared_ptr )
* Slower to allocate in comparison to variables on the stack.
* Used on demand to allocate a block of data for use by the program.
* Can have fragmentation when there are a lot of allocations and deallocations.
* In C++ or C, data created on the heap will be pointed to by pointers and allocated with new or malloc respectively.
* Can have allocation failures if too big of a buffer is requested to be allocated.
* You would use the heap if you don't know exactly how much data you will need at run time or if you need to allocate a lot of data.

&nbsp;

***

##### pointer vs. ref

* pointer 
  * can be reassigned 
  * has its own memory address and size on stack (sizeof(address_space))
  * can have ** indirection
  * can have an array of pointers
  * pointers cannot be bound to temporaries (potential unsafe for argument list)

* reference 
  * cannot be reassigned and must be assigned on initialisation
  * is an alias and shares same memory address of original variable
  * no indirection - depth of 1
  * cannot pack references in an array
  * ref can be bound to temporary variables (safer for arguments list)

&nbsp;

***

&nbsp;

http://en.cppreference.com/w/cpp/language/cv

https://stackoverflow.com/questions/79923/what-and-where-are-the-stack-and-heap#79936

https://stackoverflow.com/questions/57483/what-are-the-differences-between-a-pointer-variable-and-a-reference-variable-in

https://www.quora.com/What-is-the-difference-between-a-reference-a-pointer-and-an-iterator-Why-is-it-a-good-practice-to-use-special-iterators-instead-of-normal-variables-for-loops

https://www.autosar.org/fileadmin/user_upload/standards/adaptive/17-10/AUTOSAR_RS_CPP14Guidelines.pdf


https://stackoverflow.com/questions/2328671/constant-variables-not-working-in-header

https://stackoverflow.com/questions/3709207/c-semantics-of-static-const-vs-const

https://stackoverflow.com/questions/177437/what-does-const-static-mean-in-c-and-c

typeded alias in C++ struct

https://isocpp.org/wiki/faq/const-correctness#return-const-ref-from-const-memfn

https://stackoverflow.com/questions/4240974/when-is-it-worthwhile-to-use-bit-fields

https://stackoverflow.com/questions/10894804/forward-declaration-of-struct

https://isocpp.org/blog/2014/12/cpp-template-metaprogramming

http://blog.feabhas.com/2014/07/template-member-functions/

http://blog.feabhas.com/2014/05/an-introduction-to-c-templates/

https://isocpp.org/blog/2014/09/templates-series

https://stackoverflow.com/questions/26845538/parsing-a-binary-file-what-is-a-modern-way

https://lars-lab.jpl.nasa.gov/JPL_Coding_Standard_C.pdf

SERT C++

JSF C++

MISRA C++






