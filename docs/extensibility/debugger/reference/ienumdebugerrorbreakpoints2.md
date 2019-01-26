---
title: IEnumDebugErrorBreakpoints2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugErrorBreakpoints2
helpviewer_keywords:
- IEnumDebugErrorBreakpoints2
ms.assetid: ffdad73d-969a-45ef-9ad1-7f5d3b814018
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ac234aca006136068d1fc348627ce0003130ea89
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55009329"
---
# <a name="ienumdebugerrorbreakpoints2"></a>IEnumDebugErrorBreakpoints2
Bu arabirim, bekleyen bir kesme noktasıyla ilişkili hata kesme noktaları numaralandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEnumDebugErrorBreakpoints2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama altyapısı (DE), kesme noktaları desteğini bir parçası olarak bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Visual Studio çağrıları [CanBind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-canbind.md) bağlanamaz, kesme noktaları listesini temsil eden bir arabirimi bu alınacağı veya [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md) kesme noktaları listesini temsil eden bu arabirimi almak için bağlanamadı.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugErrorBreakpoints2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2-next.md)|Belirtilen bir sabit listesi sırası kesme noktaları hata sayısını alır.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2-skip.md)|Bir numaralandırma sıralı hata kesme noktaları, belirtilen sayıda atlar.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugerrorbreakpoints2-getcount.md)|Hata kesme noktaları sayısını bir numaralandırıcı alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim bir listesini tutar [IDebugErrorBreakpoint2](../../../extensibility/debugger/reference/idebugerrorbreakpoint2.md) arabirimleri, her biri, bağlanamadı ve neden bu bağlanamadı bir kesme noktası açıklar. Visual Studio kullanan `IEnumDebugErrorBreakpoint2` IDE'de gösterilen kesme noktalarını güncelleştirmek için arabirim.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [CanBind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-canbind.md)   
 [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)   
 [IDebugErrorBreakpoint2](../../../extensibility/debugger/reference/idebugerrorbreakpoint2.md)