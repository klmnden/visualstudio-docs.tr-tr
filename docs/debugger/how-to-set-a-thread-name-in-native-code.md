---
title: 'Nasıl yapılır: Yerel kodda iş parçacığı adı ayarlama | Microsoft Docs'
ms.date: 12/17/2018
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
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: c547dd00f7a5a31b949d22c13f305050355207c7
ms.sourcegitcommit: 22b73c601f88c5c236fe81be7ba4f7f562406d75
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56227322"
---
# <a name="how-to-set-a-thread-name-in-native-code"></a>Nasıl yapılır: Yerel kodda iş parçacığı adı ayarlama
İş parçacığı adlandırma herhangi bir sürümünü Visual Studio mümkündür. İş parçacığı adlandırma, ilgilendiğiniz iş parçacıkları tanımlamak için yararlıdır **iş parçacıkları** çalışan bir işleme hata ayıklama sırasında penceresi. İş parçacığı recognizably adlı sahip ayrıca kilitlenme dökümü İnceleme aracılığıyla ve performansını analiz etme çeşitli araçları kullanarak yakaladığında son İnceleme hata ayıklama gerçekleştirirken yararlı olabilir.

## <a name="ways-to-set-a-thread-name"></a>Bir iş parçacığı adı ayarlama yolları

İş parçacığı adı ayarlamak için iki yolu vardır. İlk aracılığıyla olduğu [SetThreadDescription](https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreaddescription) işlevi. Visual Studio hata ayıklayıcı işleme vm'sine bağlıyken belirli bir özel durum tarafından saniyedir. Her yaklaşımın avantajları ve uyarılar vardır.

Hatalarının ayıklanabileceğini belirtmekte yarar _hem_ yaklaşımları birlikte kullanılabilir, birbirinden bağımsız olarak çalışırlar mekanizmaları olduğundan, isterseniz.

### <a name="set-a-thread-name-by-using-setthreaddescription"></a>Kullanarak bir iş parçacığı adı ayarlama `SetThreadDescription`

Avantajlar:
* İş parçacığı adları olup olmadığını veya hata ayıklayıcı işleme SetThreadDescription çağrılan zaman bağlanmamış bağımsız olarak Visual Studio'da hata ayıklama sırasında görülebilir.
* Visual Studio'da kilitlenme bilgi dökümü yükleyerek son İnceleme hata ayıklama yapılırken iş parçacığı adları görülebilir.
* İş parçacığı adları da görünür gibi diğer araçları kullanarak [WinDbg](https://docs.microsoft.com/windows-hardware/drivers/debugger/debugger-download-tools) hata ayıklayıcı ve [Windows Performans Çözümleyicisi](https://docs.microsoft.com/windows-hardware/test/wpt/windows-performance-analyzer) Performans Çözümleyicisi.

Uyarılar:
* İş parçacığı adları, yalnızca Visual Studio 2017 sürüm 15.6 görünür ve üzeri.
* Bir kilitlenme hatalarını ayıklama son İnceleme döküm dosyası, iş parçacığı adları yalnızca kilitlenme Windows 10 sürüm 1607'ye, Windows Server 2016 veya sonraki Windows sürümlerinde oluşturulmuş olsa bile görülebilir.

*Örnek:*

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

### <a name="set-a-thread-name-by-throwing-an-exception"></a>Bir özel durum tarafından bir iş parçacığı adı ayarlama

Programınızda bir iş parçacığı adı ayarlama başka bir özel olarak yapılandırılmış bir özel durum atma tarafından istenen iş parçacığı adı Visual Studio hata ayıklayıcıya iletişim kurmak için yoludur.

Avantajlar:
* Visual Studio'nun tüm sürümlerinde çalışır.

Uyarılar:
* Hata ayıklayıcı özel durum tabanlı yöntemi kullanıldığında bağlıysa, yalnızca çalışır.
* Bu yöntemi kullanarak iş parçacığı adları dökümleri ya da Performans analiz araçlarını kullanılamaz.

*Örnek:*

`SetThreadName` İşlevi aşağıda gösterilen özel durum tabanlı bu yaklaşımı gösterir. İş parçacığı adı iş parçacığı için otomatik olarak kopyalanacaktır Not böylece belleği `threadName` parametresi serbest bırakılabilir sonra `SetThreadName` çağrısı tamamlandı.

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
[Çok İş Parçacıklı Uygulamaların Hatalarını Ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)  
[Hata Ayıklayıcıda Verileri Görüntüleme](../debugger/viewing-data-in-the-debugger.md)  
[Nasıl yapılır: Yerel Kodda İş Parçacığı Adı Ayarlama](../debugger/how-to-set-a-thread-name-in-managed-code.md)
