---
title: SuspendProfile | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- SuspendProfile
ms.assetid: 7c8de6e6-bb88-4353-92c3-ce7290310d61
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 6b40b37c8c0ee97b5d7e0cc33773af140bd1010b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68155619"
---
# <a name="suspendprofile"></a>SuspendProfile
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

`SuspendProfile` Yöntemi belirtilen profil oluşturma düzeyi için askıya alma/sürdürme sayacını artırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
PROFILE_COMMAND_STATUS PROFILERAPI SuspendProfile(  
                       PROFILE_CONTROL_LEVEL Level,   
                       unsigned int dwId);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `Level`  
  
 Hangi performans veri toplama uygulanabilir profili düzeyini gösterir. Aşağıdaki **PROFILE_CONTROL_LEVEL** numaralandırıcılar, hangi performans veri toplama uygulanabilir üç düzeylerinden birini belirtmek için kullanılabilir:  
  
|Numaralandırıcı|Açıklama|  
|----------------|-----------------|  
|PROFILE_GLOBALLEVEL|Genel düzeyi ayarı tüm işlemleri ve profil oluşturma, iş parçacıklarını etkiler.|  
|PROFILE_PROCESSLEVEL|İşlem düzeyi ayarı belirtilen işlemin bir parçası olan tüm iş parçacıklarını etkiler.|  
|PROFILE_THREADLEVEL|İş parçacığı düzeyi ayarı profil oluşturma, belirtilen iş parçacığı etkiler.|  
  
 `dwId`  
  
 Sistem tarafından oluşturulan işlem veya iş parçacığı tanımlayıcısı.  
  
## <a name="property-valuereturn-value"></a>Özellik Değeri/Dönüş Değeri  
 İşlevi kullanarak başarısı veya başarısızlığı gösterir **PROFILE_COMMAND_STATUS** sabit listesi. Dönüş değeri aşağıdakilerden biri olabilir:  
  
|Numaralandırıcı|Açıklama|  
|----------------|-----------------|  
|PROFILE_ERROR_ID_NOEXIST|Profil oluşturma öğesi kimliği yok.|  
|PROFILE_ERROR_LEVEL_NOEXIST|Düzey belirtilen profil yok.|  
|PROFILE_ERROR_MODE_NEVER|HİÇ işlev çağrıldığında profil oluşturma modunda ayarlandı.|  
|PROFILE_ERROR_NOT_YET_IMPLEMENTED|Profil oluşturma işlev çağrısı, profil oluşturma düzeyinde veya çağrı ve düzey henüz uygulanmadı.|  
|PROFILE_OK|Çağrı başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Askıya alma/sürdürme sayacın başlangıç değeri 0'dır. SuspendProfile yapılan her çağrı için askıya alma/sürdürme sayısı 1 ekler; her çağrı ResumeProfile 1 çıkarır.  
  
 Askıya alma/sürdürme sayısı 0'dan büyük olduğunda düzeyi için askıya alma/sürdürme durumu Kapalı'dır. Sayı 0'a eşit veya daha az olduğunda, askıya alma/sürdürme durumu açıktır.  
  
 Başlat/Durdur durumunda ve askıya alma/sürdürme durumu hem de açık olduğunda, profil oluşturma durumu düzeyi için açıktır. İş parçacığı olacak şekilde, genel işlem profili ve iş parçacığı düzeyi durumlar iş parçacığı için tüm açık.  
  
## <a name="net-framework-equivalent"></a>.NET Framework Eşdeğeri  
 Microsoft.VisualStudio.Profiler.dll  
  
## <a name="function-information"></a>İşlev bilgisi  
 Üst bilgi: Bildirilmiş VSPerf.h  
  
 İçeri aktarma kitaplığı: VSPerf.lib  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek SuspendProfile yöntemi gösterir. Bu örnekte StartProfile çağrıda işlem veya iş parçacığı tarafından tanımlanan yaptığınız varsayılmaktadır. [PROFILE_CURRENTID](../profiling/profile-currentid.md).  
  
```  
void ExerciseSuspendProfile()  
{  
    // The initial value of the Suspend/Resume counter is 0.  
    // Each call to SuspendProfile adds 1 to the  
    // Suspend/Resume count; each call  
    // to ResumeProfile subtracts 1.  
  
    // Variables used to print output  
    HRESULT hResult;  
    TCHAR tchBuffer[256];  
  
    // Declare enumeration to hold result of call  
    // to SuspendProfile  
    PROFILE_COMMAND_STATUS profileResult;  
  
    profileResult = SuspendProfile(  
        PROFILE_GLOBALLEVEL,  
        PROFILE_CURRENTID);  
  
    // Format and print result.  
    LPCTSTR pszFormat = TEXT("%s %d.\0");  
    TCHAR* pszTxt = TEXT("SuspendProfile returned");  
    hResult = StringCchPrintf(tchBuffer, 256, pszFormat,   
        pszTxt, profileResult);  
  
#ifdef DEBUG  
    OutputDebugString(tchBuffer);  
#endif  
}  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Profil Oluşturucu API Başvurusu (Yerel)](../profiling/visual-studio-profiler-api-reference-native.md)
