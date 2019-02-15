---
title: DEBUG_CUSTOM_VIEWER | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DEBUG_CUSTOM_VIEWER
helpviewer_keywords:
- DEBUG_CUSTOM_VIEWER structure
ms.assetid: 8e0ef3f0-0107-48e8-a037-6e52b4c4ed9d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fe17c8747d5c678c14561a918ddd9d62bd658841
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315839"
---
# <a name="debugcustomviewer"></a>DEBUG_CUSTOM_VIEWER
Özel bir Görüntüleyici tanımlayan bir yapı Görselleştirici yazın.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagDEBUG_CUSTOM_VIEWER {
    DWORD dwID;
    BSTR  bstrMenuName;
    BSTR  bstrDescription;
    GUID  guidLang;
    GUID  guidVendor;
    BSTR  bstrMetric;
} DEBUG_CUSTOM_VIEWER;
```

```csharp
public struct DEBUG_CUSTOM_VIEWER {
    public uint   dwID;
    public string bstrMenuName;
    public string bstrDescription;
    public Guid   guidLang;
    public Guid   guidVendor;
    public string bstrMetric;
};
```

## <a name="members"></a>Üyeler
dwID  
Birden çok İzleyici mi tarafından uygulanan görselleştiricileri ayırt etmek için bir kimlik `GUID`.

bstrMenuName  
Açılan menüde görüntülenen metin.

bstrDescription  
(Bir null değer kullanılmazsa olmalıdır) tür görselleştiricisi ve özel Görüntüleyici açıklaması.

guidLang  
Sağlayan bir ifade değerlendiricisi dili.

guidVendor  
Satıcısına sağlayan bir ifade değerlendiricisi.

bstrMetric  
Ölçüm hangi tür görselleştiricisi ve özel Görüntüleyici `CLSID` depolanır.

## <a name="remarks"></a>Açıklamalar
Bu yapının bir liste için bir çağrı tarafından döndürülen [GetCustomViewerList](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md) yöntemi (ve uzantısı tarafından [GetCustomViewerList](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewerlist.md) yöntemi).

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[GetCustomViewerList](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md)  
[GetCustomViewerList](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewerlist.md)
