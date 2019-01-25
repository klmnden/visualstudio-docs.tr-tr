---
title: THREADPROPERTY_FIELDS | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- THREADPROPERTY_FIELDS
helpviewer_keywords:
- THREADPROPERTY_FIELDS enumeration
ms.assetid: 5b88acb9-03ea-4c29-a788-f0087dccbe23
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: dc0e0f7cae4aed887809c22bda0cd6a9ed50307f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790799"
---
# <a name="threadpropertyfields"></a>THREADPROPERTY_FIELDS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Alınacak bir iş parçacığı hakkında bilgiler olduğunu belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
