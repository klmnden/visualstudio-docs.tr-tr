---
title: IActiveScript::InterruptScriptThread | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.InterruptScriptThread
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_InterruptScriptThread
ms.assetid: 2304d035-6d39-4811-acd3-8a9640fdbef6
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: aa46bc95087b3defaf739cc3473c58e29a93071c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62935514"
---
# <a name="iactivescriptinterruptscriptthread"></a>IActiveScript::InterruptScriptThread
(Bir olay havuzu, hemen bir yürütme veya bir makro çağrısı) çalışan bir betik iş yürütülmesini keser. Bu yöntem (örneğin, sonsuz bir döngüde) takılmış bir betik sonlandırmak için kullanılabilir. Temel olmayan iş parçacığından da çağrılabilir temel olmayan belirtme ana bilgisayar nesneleri veya çok kaynaklanan olmadan [Iactivescriptsite](../../winscript/reference/iactivescriptsite.md) yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT InterruptScriptThread(  
    SCRIPTTHREADID   stidThread,  // identifier of thread  
    const EXCEPINFO *pexcepinfo,  // receives error information  
    DWORD dwFlags  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `stidThread`  
 [in] Kesme ya da aşağıdaki özel iş parçacığı tanımlayıcısı değerlerden biri iş parçacığı tanıtıcısı:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|SCRIPTTHREADID_ALL|Tüm iş parçacıkları. Kesme, devam eden tüm betik yöntemleri için uygulanır. Çağıran kodun kesilmesi istedi sürece sonraki betikleştirilmiş olayı çağırarak yeniden çalıştırmak betik kodu neden olacağını unutmayın [IActiveScript::SetScriptState](../../winscript/reference/iactivescript-setscriptstate.md) SCRIPTSTATE_DISCONNECTED yöntemiyle veya SCRIPTSTATE_INITIALIZED bayrağını ayarlayın.|  
|SCRIPTTHREADID_BASE|Temel; iş parçacığı diğer bir deyişle, iş parçacığı, komut dosyası altyapısı örneği.|  
|SCRIPTTHREADID_CURRENT|Şu anda yürütülen iş parçacığı.|  
  
 `pexcepinfo`  
 [in] Adresi bir `EXCEPINFO` durdurulan betiğe bildirilen hata bilgilerini içeren yapısı.  
  
 `dwFlags`  
 [in] Kesinti ile ilişkili bayraklar seçeneği. Şu değerlerden biri olabilir:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|SCRIPTINTERRUPT_DEBUG|Destekleniyorsa, geçerli komut dosyası yürütme noktasını hata ayıklayıcı komut dosyası altyapısının girin.|  
|SCRIPTINTERRUPT_RAISEEXCEPTION|Komut dosyası altyapısının dil tarafından destekleniyorsa, özel durum işleme komut dosyası sağlar. Aksi takdirde, komut dosyası yöntemi iptal edilir ve çağırana döndürülen hata kodu; diğer bir deyişle, olay kaynağı veya makro çağırıcı.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya).|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)