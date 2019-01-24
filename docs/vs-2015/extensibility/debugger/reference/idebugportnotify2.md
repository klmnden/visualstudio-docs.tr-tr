---
title: IDebugPortNotify2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortNotify2
helpviewer_keywords:
- IDebugPortNotify2 interface
ms.assetid: 43278b79-bf16-4c08-bcf1-6f7f7a17feab
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 72e420a0601f4b78198723a2173e542d93a9206e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771699"
---
# <a name="idebugportnotify2"></a>IDebugPortNotify2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim kaydeder veya üzerinde çalıştığı bağlantı noktası ile ayıklanabilir bir program kaydını siler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPortNotify2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Özel bağlantı noktası sağlayıcısı ekleme ve kaldırma bağlantı noktasından desteklemek için bu arabirimi uygular. Genellikle uygulayan aynı nesne üzerinde uygulanan [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) arabirimi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bir çağrı [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) üzerinde `IDebugPort2` arabirimi bu arabirim döndürür. Ayrıca, bir çağrı [GetPortNotify](../../../extensibility/debugger/reference/idebugdefaultport2-getportnotify.md) bu arabirimi döndürür. Hata ayıklama altyapısı, bir parametre olarak bu arabirimi görebilirsiniz [WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md).  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortNotify2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[AddProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)|Hata ayıklaması yapılabilir bir program çalıştığı bağlantı noktası ile kaydeder.|  
|[RemoveProgramNode](../../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md)|Bir program çalıştığı bağlantı noktasından ayıklanabilir kaydını siler.|  
  
## <a name="remarks"></a>Açıklamalar  
 Özel bağlantı noktası sağlayıcısı, hata ayıklama bağlantı programlar zaman yüklü veya kaldırılmış bilmenin bir yolu olmadığı sürece, bu arabirimini uygulaması gerekir. Belirli bir bağlantı noktası üzerinden hata ayıklama için yüklenen tüm programlar bu arabirimi kullanılarak izlenir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
