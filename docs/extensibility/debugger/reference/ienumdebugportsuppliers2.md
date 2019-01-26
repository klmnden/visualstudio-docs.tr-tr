---
title: IEnumDebugPortSuppliers2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugPortSuppliers2
helpviewer_keywords:
- IEnumDebugPortSuppliers2
ms.assetid: cd0a73dc-dd25-46fd-8c4f-5b011501afeb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4e7ce7262679a1a92b54b4bd7d7deba8704237cf
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55001845"
---
# <a name="ienumdebugportsuppliers2"></a>IEnumDebugPortSuppliers2
Bu arabirim, bağlantı noktası sağlayıcıları numaralandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEnumDebugPortSuppliers2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Visual Studio, bağlantı noktası sağlayıcıları listesini temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [EnumPortSuppliers](../../../extensibility/debugger/reference/idebugcoreserver2-enumportsuppliers.md) bağlantı noktası sağlayıcıları listesi elde etmek için.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugPortSuppliers2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugportsuppliers2-next.md)|Belirtilen bir bağlantı noktası sağlayıcıları bir numaralandırma sıralı sayısını alır.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugportsuppliers2-skip.md)|Bağlantı noktası sağlayıcıları bir numaralandırma dizisinde belirtilen sayıda atlar.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugportsuppliers2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugportsuppliers2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugportsuppliers2-getcount.md)|Bağlantı noktası sağlayıcıları sayısını bir numaralandırıcı alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama altyapısı, bu arabirimi almak genellikle gerekmez.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumPortSuppliers](../../../extensibility/debugger/reference/idebugcoreserver2-enumportsuppliers.md)