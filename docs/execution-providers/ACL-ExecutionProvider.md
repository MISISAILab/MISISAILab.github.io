---
title: ARM Compute Library (ACL)
description: Instructions to execute ONNX Runtime with the ACL Execution Provider
parent: Execution Providers
nav_order: 1
redirect_from: /docs/reference/execution-providers/ACL-ExecutionProvider
---

# ACL Execution Provider
{: .no_toc }

The integration of ACL as an execution provider (EP) into ONNX Runtime accelerates performance of ONNX model workloads across Armv8 cores. [Arm Compute Library](https://github.com/ARM-software/ComputeLibrary){:target="_blank"} is an open source inference engine maintained by Arm and Linaro companies.


## Contents
{: .no_toc }

* TOC placeholder
{:toc}


## Build
For build instructions, please see the [build page](../build/eps.md#arm-compute-library).

## Usage
### C/C++
{: .no_toc }

```
Ort::Env env = Ort::Env{ORT_LOGGING_LEVEL_ERROR, "Default"};
Ort::SessionOptions sf;
bool enable_cpu_mem_arena = true;
Ort::ThrowOnError(OrtSessionOptionsAppendExecutionProvider_ACL(sf, enable_cpu_mem_arena));
```
The C API details are [here](../get-started/with-c.html).

## Performance Tuning
For performance tuning, please see guidance on this page: [ONNX Runtime Perf Tuning](../performance/tune-performance.md)

When/if using [onnxruntime_perf_test](https://github.com/microsoft/onnxruntime/tree/master/onnxruntime/test/perftest){:target="_blank"}, use the flag -e acl
