---
title: "CPU Utilization Graph | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.cv.cpu.graph"
helpviewer_keywords: 
  - "CPU Utilization GraphConcurrency Visualizer, CPU Utilization Graph"
ms.assetid: 5332fd38-622d-47a3-874f-8c2fd7a30f95
caps.latest.revision: 19
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# CPU Utilization Graph
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [CPU Utilization Graph](https://docs.microsoft.com/visualstudio/profiling/cpu-utilization-graph).  
  
The CPU Utilization graph shows the level of utilization in an app over time. The X-axis represents the duration of the trace, and the y-axis represents the number of logical cores on the system. The graph doesn't show which specific core is active at any given time. For example, if two cores are each running at 50 percent capacity for a given time period, then this view shows one logical core being utilized.  
  
## CPU Utilization graph colors  
  
-   Green indicates the utilization of the logical cores in the system by the current process.  
  
-   Light gray indicates the utilization of logical cores by other processes on the system. A high percentage of light gray in the CPU graph indicates that the system is heavily loaded by other processes and that your process is likely to be pre-empted by them. To reduce the consumption of logical cores by other processes, reduce the number of them running on the system.  
  
-   Dark gray indicates the consumption of logical cores by the system process. You can't directly control this, but it's useful to know when it's occurring because it can affect the availability of logical cores for your process.  
  
-   White indicates the availability of unused logical cores on the system. Those cores are available for your process if you can find more opportunities for parallelism.  
  
## See Also  
 [Utilization View](../profiling/utilization-view.md)   
 [Average CPU Utilization](../profiling/average-cpu-utilization.md)



