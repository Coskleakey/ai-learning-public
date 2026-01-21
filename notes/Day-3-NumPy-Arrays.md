Day 3 – NumPy Arrays, Function Signatures & Data Types
📌 What I learned today

Today focused on how NumPy creates arrays, and more importantly, why different NumPy functions exist for different use cases. Instead of memorizing syntax, I focused on understanding intent, function signatures, and numerical behavior.

🔹 Understanding Jupyter Kernels

A Jupyter kernel defines the execution environment for a notebook.

Selecting a Python 3 kernel allows NumPy, Pandas, and ML libraries to execute.

This bridges theory (math) with implementation (code).

🔹 np.arange() – Step-based array creation
np.arange(start, stop, step)


Generates values in a half-open interval [start, stop)

Best when you care about step size

Similar to Python’s range(), but returns a NumPy array

⚠️ Learned why floating-point steps can be unstable and why np.linspace is often preferred.

🔹 Function Signatures (Critical Insight)

Example:

np.arange(start_or_stop, /, stop=None, step=1, *, dtype=None)


Key takeaways:

/ → positional-only arguments

* → keyword-only arguments

This design prevents bugs and enforces clarity in scientific APIs

Understanding signatures makes NumPy (and PyTorch) documentation far easier to read.

🔹 np.linspace() – Count-based array creation
np.linspace(0, 100, 5)


Output:

[  0.  25.  50.  75. 100.]


Generates a fixed number of evenly spaced values

End value is included

Default dtype is float64 for numerical precision

🔹 Data Types (dtype)
np.linspace(0, 100, 5, dtype=int)


NumPy computes values first, then casts

Important for:

Feature engineering

Indexing

Memory efficiency

Model stability

🧠 Key Insight

Choosing between arange and linspace is not a syntax decision —
it’s a data design decision that affects numerical behavior downstream in ML models.

🚀 Next

Array reshaping

Broadcasting

Vectorized operations

How NumPy underpins PyTorch tensors
