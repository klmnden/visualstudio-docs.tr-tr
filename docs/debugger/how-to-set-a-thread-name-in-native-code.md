---
title: 'Nasıl Yapılır: Yerel kodda iş parçacığı adı ayarlama | Microsoft Docs'
ms.custom: ''
ms.date: 12/17/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- debugging [C++], threads
- SetThreadName function
- threading [Visual Studio], names
- thread names
- debugging [Visual Studio], threads
ms.assetid: c85d0968-9f22-4d69-87f4-acca2ae777b8
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- cplusplus
ms.openlocfilehash: 9226e009936d0a644a5a6fcfcaba57bc3af25d7d
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53803104"
---
# <a name="how-to-set-a-thread-name-in-native-code"></a>Nasıl Yapılır: Yerel kodda iş parçacığı adı ayarlama
İş parçacığı adlandırma herhangi bir sürümünü Visual Studio mümkündür. İş parçacığı adlandırma, iş parçacığı izlemek için kullanışlıdır **iş parçacıkları** penceresi.

## <a name="set-a-thread-name"></a>Bir iş parçacığı adı ayarlama

`SetThreadName` Ayarlama ve çalışan kod için hata ayıklayıcıyı eklediyseniz, iş parçacıkları görüntülemek için işlev yararlıdır. Visual Studio 2017 sürüm 15.6 itibaren kullanabilirsiniz [SetThreadDescription](https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreaddescription) ayarlamak ve iş parçacığı adlarını görüntülemek için işlev.

```C++
#include <windows.h>
#include <processthreadsapi.h>

int main()
{
    HRESULT r;
    r = SetThreadDescription(
        GetCurrentThread(),
        L"ThisIsMyThreadName!"
    );

    return 0;
}
```

## <a name="set-a-thread-name-using-setthreadname"></a>SetThreadName kullanarak bir iş parçacığı adı ayarlama

Programınızda bir iş parçacığı adı ayarlama için de kullanabilirsiniz `SetThreadName` , aşağıdaki kod örneğinde gösterildiği gibi işlev. İş parçacığı adı iş parçacığına kopyalanır unutmayın. böylece belleği `threadName` parametresi serbest bırakılabilir.  Bu yöntem, hata ayıklayıcı özel durum tabanlı yöntemi kullanıldığında bağlıysa, yalnızca çalışır bir özel durum tabanlı yaklaşımı kullanır. Bu yöntem kullanılarak ayarlanan iş parçacığı adı dökümleri ya da Performans analiz araçlarını kullanılamaz.

Aşağıdaki kod örneği kullanma işlemini gösterir `SetThreadName`:

```C++
//  
// Usage: SetThreadName ((DWORD)-1, "MainThread");  
//  
#include <windows.h>  
const DWORD MS_VC_EXCEPTION = 0x406D1388;  
#pragma pack(push,8)  
typedef struct tagTHREADNAME_INFO  
{  
    DWORD dwType; // Must be 0x1000.  
    LPCSTR szName; // Pointer to name (in user addr space).  
    DWORD dwThreadID; // Thread ID (-1=caller thread).  
    DWORD dwFlags; // Reserved for future use, must be zero.  
 } THREADNAME_INFO;  
#pragma pack(pop)  
void SetThreadName(DWORD dwThreadID, const char* threadName) {  
    THREADNAME_INFO info;  
    info.dwType = 0x1000;  
    info.szName = threadName;  
    info.dwThreadID = dwThreadID;  
    info.dwFlags = 0;  
#pragma warning(push)  
#pragma warning(disable: 6320 6322)  
    __try{  
        RaiseException(MS_VC_EXCEPTION, 0, sizeof(info) / sizeof(ULONG_PTR), (ULONG_PTR*)&info);  
    }  
    __except (EXCEPTION_EXECUTE_HANDLER){  
    }  
#pragma warning(pop)  
}  
```  

## <a name="see-also"></a>Ayrıca Bkz.  
 [Çok iş parçacıklı uygulamalarda hata ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)   
 [Hata ayıklayıcıda verileri görüntüleme](../debugger/viewing-data-in-the-debugger.md)   
 [Nasıl yapılır: Yönetilen kodda iş parçacığı adı ayarlama](../debugger/how-to-set-a-thread-name-in-managed-code.md)