---
title: IDebugActivateDocumentEvent2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugActivateDocumentEvent2
helpviewer_keywords:
- IDebugActivateDocumentEvent2 interface
ms.assetid: 6f37edd7-a48c-4b41-b160-dff9be63a284
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 273a0b397ea8055bb889d2700c0b651519f32f76
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54770039"
---
# <a name="idebugactivatedocumentevent2"></a>IDebugActivateDocumentEvent2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Hata ayıklama altyapısı (DE) Bu arabirim yüklenecek belge istemek için kullanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugActivateDocumentEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bir kaynak dosyası açılması gerektiğinde DE bu arabirimi uygular. Bu arabirim, birlikte çalışmak veya bir betik yorumlayıcılarını parçası olan hata ayıklama motoru tarafından uygulanır. [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) arabirim uygulandığında, bu arabirimle aynı nesne üzerinde (SDM kullanan [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) erişimi `IDebugEvent2` arabirimi).  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 DE oluşturur ve bunu açılan bir kaynak dosyanın gerektiğinde bu olay nesneyi gönderir. Olay kullanılarak gönderilen [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) ayıklanan programa eklendiğinde SDM tarafından sağlanan geri çağırma işlevi.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugActivateDocumentEvent2`.  
  
|Yöntemler|Açıklama|  
|-------------|-----------------|  
|[GetDocument](../../../extensibility/debugger/reference/idebugactivatedocumentevent2-getdocument.md)|Etkinleştirmek için belgeyi alır.|  
|[GetDocumentContext](../../../extensibility/debugger/reference/idebugactivatedocumentevent2-getdocumentcontext.md)|Belge içindeki konumunu tanımlar belge bağlamını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim kullanılan tipik bir senaryo, bir HTML sayfasında betik kodunda bir ayrıştırma hatası meydana gelirse, böylece belge ayrıştırma hatası ile görüntülenebilir DE betik bu arabirim için SDM gönderir. ' dir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
