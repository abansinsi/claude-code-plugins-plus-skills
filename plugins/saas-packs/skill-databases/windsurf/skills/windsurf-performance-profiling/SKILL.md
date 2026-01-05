---
name: "windsurf-performance-profiling"
description: |
  Profile and optimize code with AI-assisted analysis. Activate when users mention
  "performance profiling", "optimize performance", "bottleneck analysis", "profiling",
  or "performance tuning". Handles performance analysis and optimization. Use when working with windsurf performance profiling functionality. Trigger with phrases like "windsurf performance profiling", "windsurf profiling", "windsurf".
allowed-tools: "Read,Write,Edit,Bash(cmd:*),Grep"
version: 1.0.0
license: MIT
author: "Jeremy Longshore <jeremy@intentsolutions.io>"
---

# Windsurf Performance Profiling

Profile and optimize code with AI-assisted performance analysis.

## Overview

This skill enables AI-assisted performance profiling within Windsurf. Cascade analyzes profiling data to identify bottlenecks, suggest optimizations, and predict impact of changes. It integrates with language-specific profilers and helps prioritize optimization efforts based on actual performance data rather than assumptions.

## Prerequisites

- Windsurf IDE with Cascade enabled
- Profiling tools installed (Chrome DevTools, node --prof, py-spy, etc.)
- Application with performance concerns
- Baseline metrics established
- Understanding of performance targets

## Directory Structure

```
project-root/
    .windsurf/
        performance/
            profiles/
                baseline.profile.json        # Baseline performance profile
                    # Metric baselines
                    # Execution times
                    # Memory usage

                current.profile.json         # Current performance data
                    # Latest metrics
                    # Comparison to baseline
                    # Trend analysis

            reports/
                bottleneck-analysis.md       # Bottleneck identification
                    # Hot paths
                    # Memory leaks
                    # I/O bottlenecks

                optimization-plan.md         # Optimization recommendations
                    # Priority ranking
                    # Expected impact
                    # Implementation effort

                before-after.md              # Improvement documentation
                    # Metrics comparison
                    # Changes made
                    # Lessons learned

            config/
                profiler-config.json         # Profiler settings
                    # Sampling rate
                    # Tracked metrics
                    # Output format

                thresholds.json              # Performance thresholds
                    # Response time limits
                    # Memory limits
                    # CPU limits

            benchmarks/
                benchmark-suite.json         # Benchmark definitions
                    # Test scenarios
                    # Expected values
                    # Tolerance ranges

                results/
                    YYYY-MM-DD.json          # Benchmark results
                        # Execution times
                        # Memory usage
                        # Comparison data

            optimizations/
                applied/
                    optimization-001.md      # Applied optimization log
                        # Problem description
                        # Solution applied
                        # Impact measured

                pending/
                    optimization-queue.json  # Pending optimizations
                        # Identified issues
                        # Priority ranking
                        # Implementation notes
```

## Profiling Features

### Analysis
- CPU profiling
- Memory profiling
- I/O analysis
- Network profiling

### Optimization
- Bottleneck identification
- AI-suggested fixes
- Impact prediction
- Before/after comparison

## Instructions

1. **Establish Baseline**
   - Run profiler on current application
   - Document baseline metrics
   - Set performance thresholds

2. **Collect Profile Data**
   - Enable profiling for target scenarios
   - Capture representative workloads
   - Export profile data

3. **Analyze with Cascade**
   - Upload profile to Cascade
   - Identify hot paths and bottlenecks
   - Generate optimization recommendations

4. **Implement Optimizations**
   - Prioritize by impact and effort
   - Apply targeted fixes
   - Re-profile to measure improvement

5. **Document and Monitor**
   - Record before/after metrics
   - Update benchmarks
   - Set up continuous monitoring

## Output

- Profiling data and analysis
- Bottleneck identification reports
- Optimization recommendations
- Before/after comparison metrics

## Error Handling

| Error | Cause | Solution |
|-------|-------|----------|
| Profile capture failed | Profiler not configured | Check profiler installation and config |
| Incomplete data | Sampling too low | Increase sampling rate |
| Memory spike during profiling | Profiler overhead | Use sampling profiler vs instrumentation |
| Inconsistent results | Variable workload | Standardize test scenarios |
| Optimization regression | Fix introduced issue | Rollback, investigate side effects |

## Examples

**Example: Identify Memory Leaks**
Request: "Profile application for memory leaks"
Result: Memory profile showing leak sources, object retention graphs, fix suggestions

**Example: Optimize API Response Time**
Request: "Find why /api/users endpoint is slow"
Result: Profile showing database query taking 80% of time, optimization recommendations

**Example: CPU Bottleneck Analysis**
Request: "Identify CPU-intensive code paths"
Result: Flame graph with hot paths, specific function optimization suggestions

## Resources

- [Windsurf Performance Guide](https://docs.windsurf.ai/features/performance)
- [Profiling Best Practices](https://docs.windsurf.ai/guides/profiling)
- [Optimization Patterns](https://docs.windsurf.ai/guides/optimization)

## Success Criteria

- 20%+ latency reduction
- Measurable improvements documented
- Performance SLAs consistently met
