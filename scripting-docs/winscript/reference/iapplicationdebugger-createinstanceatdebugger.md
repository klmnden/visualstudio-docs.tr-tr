---
title: IApplicationDebugger::CreateInstanceAtDebugger | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IApplicationDebugger.CreateInstanceAtDebugger
apilocation:
- scrobj.dll
helpviewer_keywords:
- IApplicationDebugger::CreateInstanceAtDebugger
ms.assetid: 6763afac-c86a-4e88-9580-77108fb242fb
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 95489464128e706e755432bee991c5481f5af8bc
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63425823"
---
# <a name="iapplicationdebuggercreateinstanceatdebugger"></a>IApplicationDebugger::CreateInstanceAtDebugger
Nesneleri oluşturma hata ayıklayıcı işleminde kodla sağlar. yani giden işlem hata ayıklayıcı.  
  
> [!IMPORTANT]
> Bu yöntem bir güvenilir hata ayıklayıcı iş parçacığında rastgele nesneleri oluşturmak, güvenilmeyen kod izin verdiğinden uygulanmamalıdır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreateInstanceAtDebugger(  
   REFCLSID    rclsid,  
   IUnknown*   pUnkOuter,  
   DWORD       dwClsContext,  
   REFIID      riid,  
   IUnknown**  ppvObject  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `rclsid`  
 [in] Oluşturulacak nesne tanımlayıcısı (CLSID) sınıfı.  
  
 `pUnkOuter`  
 [in] Varsa `NULL`, nesne bir toplamanın parçası oluşturuluyor değil. Aksi takdirde, `pUnkOuter` toplama nesnesinin işaretçisidir `IUnknown` arabirimi (denetleme `IUnknown`).  
  
 `dwClsContext`  
 [in] Yürütülebilir kodu çalıştırmak için bağlam. Değerleri, sabit listesinden alınmış alınır `CLSCTX`.  
  
 `riid`  
 [in] Nesne ile iletişim kurmak için kullanılan arabirim tanımlayıcısı.  
  
 `ppvObject`  
 [out] İçinde istenen arabirim işaretçisi alır, işaretçi değişkeninin adresi `riid`. Başarılı bir geri döndürme üzerine *`ppvObject` istenen arabirim işaretçisi içerir. Başarısızlık durumunda, \* `ppvObject` içeren `NULL`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem için temsilci `CoCreateInstance`.  
  
 Yöntem henüz uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IApplicationDebugger Arabirimi](../../winscript/reference/iapplicationdebugger-interface.md)