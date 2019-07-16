---
title: IEnumDebugProcesses2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IEnumDebugProcesses2
helpviewer_keywords:
- IEnumDebugProcesses2
ms.assetid: 06a1368f-10f0-44eb-af61-e388c2327111
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d56d284d08a1c6b55318300ef7e1db1e385d584e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68178418"
---
# <a name="ienumdebugprocesses2"></a>IEnumDebugProcesses2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirim, hata ayıklama bağlantı noktasında çalışan işlemleri numaralandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEnumDebugProcesses : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Özel bağlantı noktası sağlayıcısı bir bağlantı noktasında çalışan işlemlerin bir listesini sağlamak üzere bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Visual Studio çağrıları [EnumProcesses](../../../extensibility/debugger/reference/idebugport2-enumprocesses.md) bu arabirimi elde edilir.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IEnumDebugProcesses2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugprocesses2-next.md)|Bir numaralandırma sıralı işlemlerde belirtilen sayıda alır.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugprocesses2-skip.md)|Bir numaralandırma sıralı işlemlerde belirtilen sayıda atlar.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugprocesses2-reset.md)|Bir numaralandırma sıralı başlangıç durumuna sıfırlar.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugprocesses2-clone.md)|Geçerli Numaralandırıcı aynı numaralandırma duruma içeren bir numaralandırıcı oluşturur.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugprocesses2-getcount.md)|İşlem sayısı bir numaralandırıcı alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Visual Studio doldurmak için bu arabirimi kullanan **işlemleri** penceresi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Temel arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumProcesses](../../../extensibility/debugger/reference/idebugport2-enumprocesses.md)
