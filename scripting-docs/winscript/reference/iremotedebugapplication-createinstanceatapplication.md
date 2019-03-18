---
title: IRemoteDebugApplication::CreateInstanceAtApplication | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplication.CreateInstanceAtApplication
apilocation:
- pdm.dll
helpviewer_keywords:
- IRemoteDebugApplication::CreateInstanceAtApplication
ms.assetid: d669ec80-2182-400d-87cc-7c1753315e5c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6e17c5abcb21bfaad6de948c3676d29232da66cf
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58146298"
---
# <a name="iremotedebugapplicationcreateinstanceatapplication"></a>IRemoteDebugApplication::CreateInstanceAtApplication
Nesnelerinin oluşturulması uygulama işleminde kodla sağlar. diğer bir deyişle,-işlem dışı uygulama.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT CreateInstanceAtApplication(  
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
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IRemoteDebugApplication Arabirimi](../../winscript/reference/iremotedebugapplication-interface.md)