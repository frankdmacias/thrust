---
title: minimum
parent: Generalized Identity Operations
grand_parent: Predefined Function Objects
nav_exclude: true
has_children: true
has_toc: false
---

# Struct `minimum`

<code>minimum</code> is a function object that takes two arguments and returns the lesser of the two. Specifically, it is an Adaptable Binary Function. If <code>f</code> is an object of class <code>minimum&lt;T&gt;</code> and <code>x</code> and <code>y</code> are objects of class <code>T</code><code>f(x,y)</code> returns <code>x</code> if <code>x &lt; y</code> and <code>y</code>, otherwise.


The following code snippet demonstrates that <code>minimum</code> returns its lesser argument.



```cpp
#include <thrust/functional.h>
#include <assert.h>
...
int x =  137;
int y = -137;
thrust::minimum<int> mn;
assert(y == mn(x,y));
```

**Template Parameters**:
**`T`**: is a model of <a href="https://en.cppreference.com/w/cpp/named_req/LessThanComparable">LessThan Comparable</a>.

**See**:
* <a href="/thrust/api/classes/structmaximum.html">maximum</a>
* max 
* <a href="/thrust/api/classes/structbinary__function.html">binary_function</a>

<code class="doxybook">
<span>#include <thrust/functional.h></span><br>
<span>template &lt;typename T = void&gt;</span>
<span>struct minimum {</span>
<span>public:</span><span class="doxybook-comment">&nbsp;&nbsp;/* The type of the function object's first argument.  */</span><span>&nbsp;&nbsp;typedef <i>see below</i> <b><a href="/thrust/api/classes/structminimum.html#typedef-first_argument_type">first&#95;argument&#95;type</a></b>;</span>
<br>
<span class="doxybook-comment">&nbsp;&nbsp;/* The type of the function object's second argument.  */</span><span>&nbsp;&nbsp;typedef <i>see below</i> <b><a href="/thrust/api/classes/structminimum.html#typedef-second_argument_type">second&#95;argument&#95;type</a></b>;</span>
<br>
<span class="doxybook-comment">&nbsp;&nbsp;/* The type of the function object's result;.  */</span><span>&nbsp;&nbsp;typedef <i>see below</i> <b><a href="/thrust/api/classes/structminimum.html#typedef-result_type">result&#95;type</a></b>;</span>
<br>
<span>&nbsp;&nbsp;__thrust_exec_check_disable__ __host__ constexpr __device__ T </span><span>&nbsp;&nbsp;<b><a href="/thrust/api/classes/structminimum.html#function-operator()">operator()</a></b>(const T & lhs,</span>
<span>&nbsp;&nbsp;&nbsp;&nbsp;const T & rhs) const;</span>
<span>};</span>
</code>

## Member Types

<h3 id="typedef-first_argument_type">
Typedef <code>minimum::first&#95;argument&#95;type</code>
</h3>

<code class="doxybook">
<span>typedef T<b>first_argument_type</b>;</span></code>
The type of the function object's first argument. 

<h3 id="typedef-second_argument_type">
Typedef <code>minimum::second&#95;argument&#95;type</code>
</h3>

<code class="doxybook">
<span>typedef T<b>second_argument_type</b>;</span></code>
The type of the function object's second argument. 

<h3 id="typedef-result_type">
Typedef <code>minimum::result&#95;type</code>
</h3>

<code class="doxybook">
<span>typedef T<b>result_type</b>;</span></code>
The type of the function object's result;. 


## Member Functions

<h3 id="function-operator()">
Function <code>minimum::&gt;::operator()</code>
</h3>

<code class="doxybook">
<span>__thrust_exec_check_disable__ __host__ constexpr __device__ T </span><span><b>operator()</b>(const T & lhs,</span>
<span>&nbsp;&nbsp;const T & rhs) const;</span></code>
Function call operator. The return value is <code>lhs &lt; rhs ? lhs : rhs</code>. 

