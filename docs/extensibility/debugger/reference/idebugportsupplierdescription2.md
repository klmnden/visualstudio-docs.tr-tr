---
title: IDebugPortSupplierDescription2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugPortSupplierDescription2 interface
ms.assetid: dd19b9d6-0703-44b3-9498-cedffa0ce5b7
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f6387708232c97a25ea11fc554d250e14e6b66e8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53818345"
---
# <a name="idebugportsupplierdescription2"></a>IDebugPortSupplierDescription2
Sağlar [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] içindeki metni görüntülemek için kullanıcı Arabirimi **aktarım bilgi** bölümünü **iliştirme** iletişim kutusu.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPortSupplierDescription2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirim, bağlantı noktası sağlayıcıları tarafından uygulanır.  
  
## <a name="methods"></a>Yöntemler  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugPortSupplierDescription2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetDescription](../../../extensibility/debugger/reference/idebugportsupplierdescription2-getdescription.md)|Bağlantı noktası sağlayıcısı için bir açıklama ve açıklama meta verilerini alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll