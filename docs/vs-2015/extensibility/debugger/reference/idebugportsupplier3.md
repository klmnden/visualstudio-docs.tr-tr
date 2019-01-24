---
title: IDebugPortSupplier3 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortSupplier3
helpviewer_keywords:
- IDebugPortSupplier3 interface
ms.assetid: e458cd02-2370-4435-8953-17d7a60ce152
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 46375c0b30ca563afc600d810dd27dc22882a71f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786213"
---
# <a name="idebugportsupplier3"></a>IDebugPortSupplier3
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, çağıran bir bağlantı noktası sağlayıcısı ve bağlantı noktaları (bunları diske yazarak) hata ayıklayıcı çağrıları arasında korumak daha sonra korunan Bu bağlantı noktalarının bir listesini alın belirlemek sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPortSupplier3 : IDebugPortSupplier2  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Özel bağlantı noktası sağlayıcısı kalıcı veya bağlantı noktası bilgilerini diske kaydedilirken desteklemek için bu arabirimi uygular. Bu arabirim aynı nesne üzerinde uygulanması gereken [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md) arabirimi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Çağrı [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) üzerinde `IDebugPortSupplier2` arabirimi bu arabirim elde edilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Devralınan yöntemleri yanı sıra [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md) arabirimi bu arabirim, aşağıdakileri destekler:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[CanPersistPorts](../../../extensibility/debugger/reference/idebugportsupplier3-canpersistports.md)|Bağlantı noktası sağlayıcısı bağlantı noktası (bunları diske yazarak) hata ayıklayıcı çağrıları arasında kalıcı olup olmadığını döndürür.|  
|[EnumPersistedPorts](../../../extensibility/debugger/reference/idebugportsupplier3-enumpersistedports.md)|Numaralandırılacak Bu bağlantı noktası sağlayıcısı tarafından diske yazılan tüm bağlantı noktaları üzerinden kullanılabilir bir nesne döndürür.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bağlantı noktası sağlayıcısı çağrıları arasında küçük bağlantı noktalarına devam ediyorsa, bu arabirimi uygulamalıdır. Bağlantı noktası, bağlantı noktası sağlayıcısı örneği ve bağlantı noktası sağlayıcısı kaldırıldığında diske yazılan yüklenmelidir.  
  
 Hata ayıklama altyapısı genellikle bağlantı noktası sağlayıcısı ile etkileşime girmez ve bu arabirim için herhangi bir kullanıma sahip olur.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)
