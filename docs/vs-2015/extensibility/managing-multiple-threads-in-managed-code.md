---
title: Yönetilen kodda birden çok iş parçacığını yönetme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
ms.assetid: 59730063-cc29-4dae-baff-2234ad8d0c8f
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 4e7198623283fa3ef9c82d6a39a1f7c1db6c760c
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63433041"
---
# <a name="managing-multiple-threads-in-managed-code"></a>Yönetilen Kodda Birden Çok İş Parçacığını Yönetme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio UI iş parçacığı dışında iş parçacığı üzerinde yürütülen işlemler zaman uyumsuz yöntemleri çağırır veya yönetilen bir VSPackage uzantısı varsa, aşağıda verilen yönergeleri izlemelidir. Bunu tamamlamak için başka bir iş parçacığı üzerinde iş için beklemesi gerekmez çünkü UI iş parçacığı hızlı yanıt veren tutabilirsiniz. Yığın yer kaplar ek iş parçacıkları sahip olmadığınızdan, kodunuzu daha verimli hale getirebilir ve daha güvenilir ve daha kolay Kilitlenmeler ve kilitlenmelerini önlemek için hata ayıklama yapabilirsiniz.  
  
 Genel olarak, farklı bir iş parçacığı UI iş parçacığından geçebilir veya bunun tersi de geçerlidir. Yöntem döndürüldüğünde, geçerli iş parçacığı içinden verilmiş olan başlangıçtaki parçacığıdır.  
  
> [!IMPORTANT]
> API'leri aşağıdaki kılavuzları kullanın <xref:Microsoft.VisualStudio.Threading> ad alanı, özellikle de <xref:Microsoft.VisualStudio.Threading.JoinableTaskFactory> sınıfı. Bu ad alanındaki API'leri yeni [!INCLUDE[vs_dev12](../includes/vs-dev12-md.md)]. Örneği alabileceğiniz bir <xref:Microsoft.VisualStudio.Threading.JoinableTaskFactory> gelen <xref:Microsoft.VisualStudio.Shell.ThreadHelper> özelliği `ThreadHelper.JoinableTaskFactory`.  
  
## <a name="switching-from-the-ui-thread-to-a-background-thread"></a>UI iş parçacığından bir arka plan iş parçacığına geçiş  
  
1. UI iş parçacığı üzerinde olan ve arka plan iş parçacığında zaman uyumsuz iş yapmak istiyorsanız Task.Run() kullanın:  
  
    ```csharp  
    await Task.Run(async delegate{  
        // Now you’re on a separate thread.  
    });  
    // Now you’re back on the UI thread.  
  
    ```  
  
2. UI iş parçacığı üzerinde olan ve bir arka plan iş parçacığında kullanımı iş gerçekleştirirken zaman uyumlu olarak engellemek istiyorsanız <xref:System.Threading.Tasks.TaskScheduler> özelliği `TaskScheduler.Default` içinde <xref:Microsoft.VisualStudio.Threading.JoinableTaskFactory.Run%2A>:  
  
    ```csharp  
    // using Microsoft.VisualStudio.Threading;  
    ThreadHelper.JoinableTaskFactory.Run(async delegate {  
        await TaskScheduler.Default;  
        // You're now on a separate thread.  
        DoSomethingSynchronous();  
        await OrSomethingAsynchronous();  
    });  
    ```  
  
## <a name="switching-from-a-background-thread-to-the-ui-thread"></a>Arka plan iş parçacığından UI iş parçacığına değiştirme  
  
1. Arka plan iş parçacığında işiniz ve kullanıcı Arabirimi iş parçacığı kullanımı hakkında bir şey istiyorsanız <xref:Microsoft.VisualStudio.Threading.JoinableTaskFactory.SwitchToMainThreadAsync%2A>:  
  
    ```csharp  
    // Switch to main thread  
    await ThreadHelper.JoinableTaskFactory.SwitchToMainThreadAsync();  
    ```  
  
     Kullanabileceğiniz <xref:Microsoft.VisualStudio.Threading.JoinableTaskFactory.SwitchToMainThreadAsync%2A> UI iş parçacığına geçiş yapmak için yöntemi. Bu yöntem, devamlılığın geçerli zaman uyumsuz metot ile UI iş parçacığına bir ileti gönderir ve ayrıca doğru önceliğini ayarlamak ve kilitlenmeleri önlemek için iş parçacığı çerçevesi geri kalanı ile iletişim kurar.  
  
     Arka plan iş parçacığı yönteminizi zaman uyumsuz değildir ve zaman uyumsuz yapamazsınız, kullanmaya devam edebilirsiniz `await` iş sarmalama tarafından UI iş parçacığına geçiş yapmak için söz dizimi <xref:Microsoft.VisualStudio.Threading.JoinableTaskFactory.Run%2A>, bu örnekte olduğu gibi:  
  
    ```csharp  
    ThreadHelper.JoinableTaskFactory.Run(async delegate {  
        // Switch to main thread  
        await ThreadHelper.JoinableTaskFactory.SwitchToMainThreadAsync();  
        // Do your work on the main thread here.  
    });  
    ```
