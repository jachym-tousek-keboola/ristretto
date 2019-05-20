# ring

Striped, lossy ring buffers meant for MPSC work.

## benchmarks

* Benchmarks are ran on an Intel i7-8700K (3.7GHz 6-core)
* Ring size: 128 (uint64s)
* Stripe count: 16
* **NOTE:** MB/s is operations per second (not megabytes per second)

```
BenchmarkBuffer-12             	200000000	         7.63 ns/op	 131.14 MB/s	       8 B/op	       0 allocs/op
BenchmarkBufferParallel-12     	50000000	        30.8 ns/op	  32.44 MB/s	       7 B/op	       0 allocs/op
BenchmarkBuffers-12            	100000000	        10.2 ns/op	  97.96 MB/s	       8 B/op	       0 allocs/op
BenchmarkBuffersParallel-12    	100000000	        21.0 ns/op	  47.72 MB/s	       8 B/op	       0 allocs/op
```