[Back to the projects list](../../)

<!-- For information on how to write GitHub .md files see https://guides.github.com/features/mastering-markdown/ -->

# Improve template matching in SpikeInterface

## Key Investigators

Pierre Yger
Samuel Garcia
Joulien Boussard


## Project Description

## Objectives

Many spike sorters use *template matching* aka *peeler* aka *deconvolution* as a final step in 
the spike sorting pipeline. It is one of the best option to handle the spike collision issue.

There are many algorithms that can be used for that steps.

SpikeInterface already includes 3 of then:
  * tridesclous strategy
  * spyking-cicus strategy
  * cicus-omp (orthogonal matching pursuit) strategy

These 3 methods give decent results, but bencmarks are still limited.

The hackathon would be an oportunity to improve the existing strategies and port more methods for a more systematic and complete benchmark.


## Approach and Plan

Implement methods from other sorter:

 * [ ] YASS
 * [ ] Kilosort
 * [ ] HDSort

Make notebooks to report benchmarks in various conditions:
  * [ ] low/high channel count
  * [ ] stationary vs drift dataset
  * [ ] low/high spike collisions
  * [ ] low/high bursting modulation

  
## Progress

During the workshop, we mostly focus on developping benchmarks for the already implemented peeler, in order to be able to quickly test the performances on various
recordings/probe layout. The module has been refactored such that every matching engine has now its own files, and thus the readibility of the code has been 
improved. A `BenchmarkMatching` object has been created in order to handle all the comparisons/tests of performances. A notebook providing some examples of how to 
run/benchmark the various peeler has been updated

## Next steps

More visualization could be done, and a more intensive comparisons depending on various recordings/probes should be done. For exmaple, the scaling to NeuroPixel 
recordings has not been tested yet, and also some more *template matching* engines should be implemented.

## Materials


## Background and References


[tridesclous engine](https://github.com/tridesclous/tridesclous)
[spyking-circus engine](https://github.com/spyking-circus/spyking-circus)
[Differences between Matching pursuit and Orthogonal Matching pursuit](https://en.wikipedia.org/wiki/Matching_pursuit)

