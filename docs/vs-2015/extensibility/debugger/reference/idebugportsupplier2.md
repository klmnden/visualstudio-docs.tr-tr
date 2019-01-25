---
title: IDebugPortSupplier2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortSupplier2
helpviewer_keywords:
- IDebugPortSupplier2 interface
ms.assetid: 37067324-2ea6-4a01-8829-a6e9c7a70068
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b6d9c3f8b45affd192d4109db08454345dcd0814
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54805041"
---
# <a name="idebugportsupplier2"></a>IDebugPortSupplier2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim bağlantı noktalarına oturum hata ayıklama Yöneticisi (SDM) sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPortSupplier2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Özel bağlantı noktası sağlayıcısı bağlantı noktası sağlayıcısı temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bir çağrı `CoCreateInstance` ile bir bağlantı noktası tedarikçi `GUID` (Bu, bu arabirimi sağlamak için normal şekilde) Bu arabirim döndürür. Örneğin:  
  
```cpp#  
IDebugPortSupplier2 *GetPortSupplier(GUID *pPortSupplierGuid)  
{  
    IDebugPortSupplier2 *pPS = NULL;  
    if (pPortSupplierGuid != NULL) {  
        CComPtr<IDebugPortSupplier2> spPortSupplier;  
        spPortSupplier.CoCreateInstance(*pPortSupplierGuid);  
        if (spPortSupplier != NULL) {  
            pPS = spPortSupplier.Detach();  
        }  
    }  
    return (pPS);  
}  
```  
  
 Bir çağrı [GetPortSupplier](../../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md) tarafından kullanılan geçerli bağlantı noktası sağlayıcısı gösteren bu bir arabirim döndürür [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)].  
  
 [GetPortSupplier](../../../extensibility/debugger/reference/idebugport2-getportsupplier.md) bağlantı noktası oluşturulan bağlantı noktası sağlayıcısı temsil eden bu arabirimi döndürür.  
  
 [IEnumDebugPortSuppliers2](../../../extensibility/debugger/reference/ienumdebugportsuppliers2.md) listesini temsil `IDebugPortSupplier` arabirimleri ( `IEnumDebugPortSuppliers` arabirimi öğesinden alınan [EnumPortSuppliers](../../../extensibility/debugger/reference/idebugcoreserver2-enumportsuppliers.md), tüm bağlantı noktası sağlayıcıları temsil eden ilekayıtlı[!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)]).  
  
 Hata ayıklama altyapısı genellikle bağlantı noktası sağlayıcısı ile etkileşime girmez.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortSupplier2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetPortSupplierName](../../../extensibility/debugger/reference/idebugportsupplier2-getportsuppliername.md)|Bağlantı sağlayıcı adını alır.|  
|[GetPortSupplierId](../../../extensibility/debugger/reference/idebugportsupplier2-getportsupplierid.md)|Bağlantı noktası tedarikçi tanımlayıcısını alır.|  
|[GetPort](../../../extensibility/debugger/reference/idebugportsupplier2-getport.md)|Bir bağlantı noktasına bağlantı noktası sağlayıcısı alır.|  
|[EnumPorts](../../../extensibility/debugger/reference/idebugportsupplier2-enumports.md)|Mevcut bağlantı noktalarını listeler.|  
|[CanAddPort](../../../extensibility/debugger/reference/idebugportsupplier2-canaddport.md)|Bağlantı noktası sağlayıcısı yeni bağlantı noktaları ekleme desteklediğini doğrular.|  
|[AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)|Bir bağlantı noktası ekler.|  
|[RemovePort](../../../extensibility/debugger/reference/idebugportsupplier2-removeport.md)|Bir bağlantı noktası kaldırır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bağlantı noktası sağlayıcısı adı ve kimliği ile kendisini tanımlamak, ekleyin ve bağlantı noktalarını kaldırın ve bağlantı noktası sağlayıcısı sağlayan tüm bağlantı noktalarını listele.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [GetPortSupplier](../../../extensibility/debugger/reference/idebugport2-getportsupplier.md)   
 [GetPortSupplier](../../../extensibility/debugger/reference/idebugcoreserver2-getportsupplier.md)   
 [IEnumDebugPortSuppliers2](../../../extensibility/debugger/reference/ienumdebugportsuppliers2.md)
