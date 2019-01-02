---
title: MarkProfile | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- MarkProfile
ms.assetid: 54dac8c8-c8ee-4023-af27-b25466e3a6ec
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5d079310fa8fa579f05e927eb37a0cbd6f2c8cca
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53853755"
---
# <a name="markprofile"></a>MarkProfile
`MarkProfile` Yöntemi profili işareti ekler. *Vsp* dosya. Profil oluşturma için iş parçacığı içeren `MarkProfile` işlevi eklenecek işareti için açık olması gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
PROFILE_COMMAND_STATUS PROFILERAPI MarkProfile( long lMarker );  
```  
  
#### <a name="parameters"></a>Parametreler  
 `lMarker`  
  
 Eklenecek işaretçisi. İşaretin değerinden büyük veya 0 (sıfır) eşit olmalıdır.  
  
## <a name="property-valuereturn-value"></a>Özellik değeri/dönüş değeri  
 İşlevi kullanarak başarısı veya başarısızlığı gösterir **PROFILE_COMMAND_STATUS** sabit listesi. Dönüş değeri aşağıdakilerden biri olabilir:  
  
|Numaralandırıcı|Açıklama|  
|----------------|-----------------|  
|MARK_ERROR_MARKER_RESERVED|Parametresi veya 0'a eşit olan küçük. Bu değerler ayrılmıştır. Açıklama ve işareti kaydedilmez.|  
|MARK_ERROR_MODE_NEVER|HİÇ işlev çağrıldığında profil oluşturma modunda ayarlandı. Açıklama ve işareti kaydedilmez.|  
|MARK_ERROR_MODE_OFF|İşlev çağrıldığında, profil oluşturma modunda OFF olarak ayarlandı. Açıklama ve işareti kaydedilmez.|  
|MARK_ERROR_NO_SUPPORT|Bu bağlamda işareti desteği yok. Açıklama ve işareti kaydedilmez.|  
|MARK_ERROR_OUTOFMEMORY|Bellek olayı kaydetmek kullanılabilir değildi. Açıklama ve işareti kaydedilmez.|  
|MARK_TEXTTOOLONG|Dize en fazla 256 karakter aşıyor. Açıklama dizesi kesilmiş ve işareti ve yorum kaydedilir.|  
|MARK_OK|MARK_OK tamamlandığını bildiren döndürülür.|  
  
## <a name="remarks"></a>Açıklamalar  
 Değeri işareti eklenir. *vsp* dosyası her zaman kod MarkProfile işlevi içeren iş parçacığı profili varsa çalışır. Birden çok kez MarkProfile çağırabilirsiniz.  
  
 Profil işaretleri kapsam içinde geneldir. Örneğin, bir iş parçacığında eklenen bir profili işareti başlangıç veya bitiş içinde herhangi bir iş parçacığı bir veri parçasının işaretlemek için kullanılabilir. *vsp* dosya.  
  
 İşaretler ve açıklama işareti komutu veya API işlevleri (CommentMarkAtProfile, CommentMarkProfile veya MarkProfile) ile eklendiğinde işareti profili işlevi içeren iş parçacığı profil durumu olmalıdır.  
  
> [!IMPORTANT]
>  MarkProfile yöntemi yalnızca izleme profil ile kullanılmalıdır.  
  
## <a name="net-framework-equivalent"></a>.NET framework eşdeğeri  
 *Microsoft.VisualStudio.Profiler.dll*  
  
## <a name="function-information"></a>İşlev bilgisi  
 Üst bilgi: Bildirilen *VSPerf.h*  
  
 İçeri aktarma kitaplığı: *VSPerf.lib*  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod MarkProfile işlevi gösterir.  
  
```cpp  
void ExerciseMarkProfile()  
{  
    // Declare and initialize variables to pass to   
    // MarkProfile.  The values of these parameters   
    // are assigned based on the needs of the code;  
    // and for the sake of simplicity in this example,   
    // the variables are assigned arbitrary values.  
    int markId = 03;  
  
    // Declare enumeration to hold return value of   
    // call to MarkProfile.  
    PROFILE_COMMAND_STATUS markResult;  
  
    // Variables used to print output.  
    HRESULT hResult;  
    TCHAR tchBuffer[256];  
  
    markResult = MarkProfile(markId);  
  
    // Format and print result.  
    LPCTSTR pszFormat = TEXT("%s %d.\0");  
    TCHAR* pszTxt = TEXT("MarkProfile returned");  
    hResult = StringCchPrintf(tchBuffer, 256, pszFormat,   
        pszTxt, markResult);  
  
#ifdef DEBUG  
    OutputDebugString(tchBuffer);  
#endif  
}  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio profil oluşturucu API Başvurusu (yerel)](../profiling/visual-studio-profiler-api-reference-native.md)