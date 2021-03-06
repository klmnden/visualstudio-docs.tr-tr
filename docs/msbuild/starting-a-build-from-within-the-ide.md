---
title: IDE içinden derleme başlatma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- build
ms.assetid: 936317aa-63b7-4eb0-b9db-b260a0306196
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ae3478aef733d106fa075a51edce4af91b404149
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62939408"
---
# <a name="start-a-build-from-within-the-ide"></a>IDE içinden derleme Başlat
Özel proje sistemleri kullanmalıdır <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildManagerAccessor> yapıları başlatmak için. Bu makalede, bu gereksinim nedenlerini açıklar ve yordamı açıklar.

## <a name="parallel-builds-and-threads"></a>Paralel yapılar ve iş parçacıkları
 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Ortak kaynaklara erişim için dolayımlama gerektiren paralel yapılar sağlar. Proje sistemleri yapıları zaman uyumsuz olarak çalıştırabilirsiniz, ancak bu tür sistemleri telefonla geri arama içinden yapı işlevlerini çağırmamalıdır.

 Proje sistemi ortam değişkenlerini değiştiriyorsa, yapı Outofproc olarak ayarlaması gerekir. Bu gereksinim, bunlar işlemde düğüm gerektirdiklerinden, ana bilgisayar nesnelerini kullanamayacağınız anlamına gelir.

## <a name="use-ivsbuildmanageraccessor"></a>Use IVSBuildManagerAccessor
 Aşağıdaki kod, proje sistemi bir derlemeyi başlatmak için kullanabileceğiniz bir yöntemin anahatlarını vermektedir:

```csharp

public bool Build(Project project, bool isDesignTimeBuild)
{
    // Get the accessor from the IServiceProvider interface for the
    // project system
    IVsBuildManagerAccessor accessor =
        serviceProvider.GetService(typeof(SVsBuildManagerAccessor)) as
        IVsBuildManagerAccessor;
    bool releaseUIThread = false;
    try
    {
        if(accessor != null)
        {
            // Claim the UI thread under the following conditions:
            // 1. The build must use a resource that uses the UI thread
            // or,
            // 2. The build requires the in-proc node AND waits on the
            // UI thread for the build to complete
            if(NeedsUIThread)
            {
                int result = accessor.ClaimUIThreadForBuild();
                if(result != S_OK)
                {
                     // Not allowed to claim the UI thread right now
                     return false;
                }
                releaseUIThread = true;
             }
             if(isDesignTimeBuild)
             {
// Start the design time build
                  int result = accessor.BeginDesignTimeBuild();
                  if(result != S_OK)
                  {
                      // Not allowed to begin a design-time build at
                      // this time. Try again later.
                      return false;
                  }
             }
         }
         bool buildSucceeded = false;
         // perform project-system specific build set up tasks
         // Create your BuildRequestData
         // This assumes a IHostServices variable (hostServices) set
   // to your host services. If you don't use a project instance
         // (you build from a file for example) then use another
         // constructor.
         BuildRequestData requestData = new
             BuildRequestData(project.CreateProjectInstance(),
             "myTarget", hostServices,
             BuildRequestData.BuildRequestDataFlags.None);
         // Mark your your submission as Pending
         BuildSubmission submission =
              BuildManager.DefaultBuildManager.
              PendBuildRequest(requestData);
         // Register the loggers in BuildLoggers
         if (accessor != null)
         {
               foreach (ILogger logger in BuildLoggers)
               {
                    accessor.RegisterLogger(submission.SubmissionId,
                        logger);
               }
         }
         BuildResult buildResult = submission.Execute();
         return buildResult;
     }
     // Clean up resources
     finally
     {
         if(accessor != null)
         {
             // Unregister the loggers, if necessary.
             accessor.UnregisterLoggers(submission.SubmissionId);
             // Release the UI thread, if used
             if(releaseUIThread)
             {
                  accessor.ReleaseUIThreadForBuild();
             }
             // End the design time build, if used
             if(isDesignTimeBuild)
             {
                  accessor.EndDesignTimeBuild();
             }
         }
     }
}
```