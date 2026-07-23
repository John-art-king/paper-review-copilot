# Edge Deployment and Model Conversion Checklist

Use this checklist for papers involving model formats, conversion, graph optimization, compilers, quantization, inference runtimes, accelerators, or edge deployment.

## Map the System Boundary

Place the paper's contribution in one or more distinct layers:

- framework export and model interchange;
- format conversion and semantic validation;
- graph IR, lowering, and compiler optimization;
- kernel generation and scheduling;
- inference runtime, partitioning, and fallback;
- device drivers, accelerator libraries, and hardware.

Name the interfaces between layers. Do not treat serialization success, compilation success, numerical correctness, runtime execution, and hardware acceleration as equivalent outcomes. Do not credit a compiler or runtime paper with format-conversion novelty unless semantic interchange or conversion is an explicit contribution.

## Define the Deployment Contract

Extract:

- source framework and model version;
- source and target formats, IRs, and opset versions;
- target runtime, hardware, OS, drivers, and accelerator libraries;
- input shapes, dynamic dimensions, batch size, precision, and preprocessing;
- quality tolerance and numerical equivalence criteria;
- latency, throughput, memory, storage, power, energy, and startup constraints.

Treat a conversion result as incomplete when the target device or runtime contract is unspecified.

## Inspect Conversion Correctness

Check:

- operator coverage and unsupported-operator fallbacks;
- graph rewrites, constant folding, fusion, layout changes, and shape inference;
- custom operators and runtime-specific extensions;
- dynamic control flow, variable-length inputs, and dynamic shapes;
- preprocessing and postprocessing equivalence;
- weight transformation, precision conversion, calibration, and rounding behavior;
- output agreement across representative, boundary, and adversarial inputs;
- tolerance definition per output rather than one unexplained global threshold.

Separate successful serialization from semantic correctness and successful runtime execution.

## Inspect Performance Evidence

Require enough detail to reproduce measurements:

- device model, CPU/GPU/NPU frequencies, thermal state, and power mode;
- runtime and dependency versions;
- thread count, affinity, delegates/providers, and compiler flags;
- warm-up policy, run count, synchronization, and cache state;
- cold-start and steady-state latency;
- p50 and tail latency when the use case is interactive;
- throughput at stated batch size;
- peak and resident memory, model size, and temporary workspace;
- energy per inference or power under load when energy efficiency is claimed;
- accuracy or task quality after conversion and optimization.

Reject desktop or simulator measurements as sufficient evidence for an edge-device claim unless the paper clearly limits its scope.

## Check Baseline Fairness

Compare against:

- direct export or vendor-recommended conversion;
- the closest compiler or conversion pipeline;
- the same runtime without the proposed optimization;
- matched precision, batch, input size, hardware, threads, and quality target;
- end-to-end latency as well as isolated kernel or compiler time when relevant.

Account for conversion time, calibration cost, generated artifact size, and unsupported-model failure rate when the paper claims a practical tool or system.

## Classify the Contribution

Possible substantive contributions include:

- broader semantic operator coverage with verified correctness;
- a new IR or rewrite that enables previously unsupported deployment;
- hardware-aware optimization that moves a measured quality-cost frontier;
- automatic partitioning, fallback, or scheduling with robust gains;
- cross-format verification or error localization;
- a benchmark exposing conversion correctness and portability failures;
- an end-to-end system that materially reduces engineering effort and is evaluated on realistic model diversity.

Common overclaims include:

- wrapping existing converters behind one interface;
- reporting conversion success without numerical validation;
- testing only one model family or one favorable device;
- claiming portability while using target-specific custom operators;
- claiming acceleration without matched precision and quality;
- reporting average latency without warm-up, variance, or thermal controls;
- ignoring preprocessing, postprocessing, and host-device transfer.

## Derive Research Opportunities

Look for:

- unsupported operators or graph patterns that cluster by model family;
- conversion errors that could be localized automatically;
- quality drift under mixed precision or quantization;
- dynamic-shape and control-flow failures;
- mismatch between framework semantics and target runtime semantics;
- performance portability across heterogeneous edge hardware;
- cost-aware backend selection under memory, latency, and energy constraints;
- reproducible benchmarks covering correctness, robustness, and deployment cost;
- graceful fallback when full acceleration is impossible;
- provenance and explainability for graph transformations.

Turn each opportunity into a testable hypothesis with representative models, devices, baselines, correctness tolerances, and end-to-end metrics.
