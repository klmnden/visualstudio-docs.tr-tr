---
title: IDebugProgramEx2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProgramEx2
helpviewer_keywords:
- IDebugProgramEx2 interface
ms.assetid: 663359ed-635a-4539-addb-0cc52f19d1bd
caps.latest.revision: 19
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 9858b205f3bf581f2595ea645dcea700a382a6b1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54790808"
---
# <a name="idebugprogramex2"></a>IDebugProgramEx2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, hata ayıklama Yöneticisi (SDM), bir programa ekledikten ve programla ilişkili program düğümünü Al oturum sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProgramEx2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Özel bağlantı noktası sağlayıcısı aynı nesne üzerinde bu arabirimi uygulayan [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) aynı anda tüm oturumları izlemek bağlantı noktası sağlayıcısı izin vererek bağlı durumdayken, bir programa ekledikten SDM izin vermek için arabirimi Program. Seçerse bu özel bağlantı noktası sağlayıcısı bu arabirim uygulayabilir.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 SDM çağrıları [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) üzerinde bir `IDebugProgram2` programlar ekli oturumları izlemek için bu arabirimi almak için arabirim.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramEx2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Attach](../../../extensibility/debugger/reference/idebugprogramex2-attach.md)|Bir program bir oturumuna ekler.|  
|[GetProgramNode](../../../extensibility/debugger/reference/idebugprogramex2-getprogramnode.md)|Bir programla ilişkili program düğümünü alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, SDM ve program özeldir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Portpriv.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
