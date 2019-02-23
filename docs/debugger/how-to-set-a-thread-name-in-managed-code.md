---
title: 'Nasıl yapılır: Yönetilen kodda iş parçacığı adı ayarlama | Microsoft Docs'
ms.date: 04/27/2017
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Thread.Name property
- threading [Visual Studio], names
- thread names
- debugging [Visual Studio], threads
ms.assetid: c0c4d74a-0314-4b71-81c9-b0b019347ab8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: d0954ffadd1bb1b09d7294be673f961ca2f18058
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56713093"
---
# <a name="how-to-set-a-thread-name-in-managed-code"></a>Nasıl yapılır: Yönetilen kodda iş parçacığı adı ayarlama
İş parçacığı adlandırma herhangi bir sürümünü Visual Studio mümkündür. İş parçacığı adlandırma, iş parçacığı izlemek için kullanışlıdır **iş parçacıkları** penceresi.

 Yönetilen kodda iş parçacığı adı ayarlamak için kullanın <xref:System.Threading.Thread.Name%2A> özelliği.

## <a name="example"></a>Örnek

```csharp
public class Needle
{
    // This method will be called when the thread is started.
    public void Baz()
    {
        Console.WriteLine("Needle Baz is running on another thread");
    }
}

public void Main()
{
    Console.WriteLine("Thread Simple Sample");
    Needle oNeedle = new Needle();
    // Create a Thread object.
    System.Threading.Thread oThread = new System.Threading.Thread(oNeedle.Baz);
    // Set the Thread name to "MyThread".
    oThread.Name = "MyThread";
    // Starting the thread invokes the ThreadStart delegate
    oThread.Start();
}
```

```VB
Public Class Needle
    ' This method will be called when the thread is started.
    Sub Baz()
        Console.WriteLine("Needle Baz is running on another thread")
    End Sub
End Class

Sub Main()
    Console.WriteLine("Thread Simple Sample")
    Dim oNeedle As New Needle()
   ' Create a Thread object.
    Dim oThread As New System.Threading.Thread(AddressOf oNeedle.Baz)
    ' Set the Thread name to "MyThread".
    oThread.Name = "MyThread"
    ' Starting the thread invokes the ThreadStart delegate
    oThread.Start()
End Sub
```

## <a name="see-also"></a>Ayrıca Bkz.
- [DDebug çok iş parçacıklı uygulamalar](../debugger/debug-multithreaded-applications-in-visual-studio.md)
- [Nasıl yapılır: Yerel Kodda İş Parçacığı Adı Ayarlama](../debugger/how-to-set-a-thread-name-in-native-code.md)