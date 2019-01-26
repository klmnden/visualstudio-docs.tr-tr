---
title: THREADPROPERTY_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- THREADPROPERTY_FIELDS
helpviewer_keywords:
- THREADPROPERTY_FIELDS enumeration
ms.assetid: 5b88acb9-03ea-4c29-a788-f0087dccbe23
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b181cc341ea0297cc78c0970a5de64df830dc3e6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54937541"
---
# <a name="threadpropertyfields"></a>THREADPROPERTY_FIELDS
Alınacak bir iş parçacığı hakkında bilgiler olduğunu belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_THREADPROPERTY_FIELDS {   
   TPF_ID           = 0x0001,  
   TPF_SUSPENDCOUNT = 0x0002,  
   TPF_STATE        = 0x0004,  
   TPF_PRIORITY     = 0x0008,  
   TPF_NAME         = 0x0010,  
   TPF_LOCATION     = 0x0020,  
   TPF_ALLFIELDS    = 0xffffffff  
};  
typedef DWORD THREADPROPERTY_FIELDS;  
```  
  
```csharp  
public enum enum_THREADPROPERTY_FIELDS {   
   TPF_ID           = 0x0001,  
   TPF_SUSPENDCOUNT = 0x0002,  
   TPF_STATE        = 0x0004,  
   TPF_PRIORITY     = 0x0008,  
   TPF_NAME         = 0x0010,  
   TPF_LOCATION     = 0x0020,  
   TPF_ALLFIELDS    = 0xffffffff  
};  
```  
  
## <a name="members"></a>Üyeler  
 TPF_ID  
 Başlat/kullanım `dwThreadId` alanını [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md) yapısı.  
  
 TPF_SUSPENDCOUNT  
 Başlat/kullanım `dwSuspendCount` alanını `THREADPROPERTIE`S yapısı.  
  
 TPF_STATE  
 Başlat/kullanım `dwThreadState` alanını `THREADPROPERTIE`S yapısı.  
  
 TPF_PRIORITY  
 Başlat/kullanım `bstrPriority` alanını `THREADPROPERTIE`S yapısı.  
  
 TPF_NAME  
 Başlat/kullanım `bstrName` alanını `THREADPROPERTIE`S yapısı.  
  
 TPF_LOCATION  
 Başlat/kullanım `bstrLocation` alanını `THREADPROPERTIE`S yapısı.  
  
 TPF_ALLFIELDS  
 Tüm alanları belirtir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu değerleri bir bağımsız değişken olarak geçirilen [GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2-getthreadproperties.md) hangi alanları göstermek için yöntemi [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md) yapısı olan başlatılacak.  
  
 Bu değerleri de kullanılan `dwFields` üyesi `THREADPROPERTIES` yapısı hangi alanların kullanılan ve geçerli olduğunu belirtmek için.  
  
 Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md)   
 [GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2-getthreadproperties.md)