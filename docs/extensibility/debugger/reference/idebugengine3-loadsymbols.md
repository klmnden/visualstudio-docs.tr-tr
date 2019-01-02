---
title: IDebugEngine3::LoadSymbols | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugEngine3::LoadSymbols
helpviewer_keywords:
- IDebugEngine3::LoadSymbols
ms.assetid: c846a440-1d91-4d48-b8f1-82e902ae152b
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: b74b4303d85364e5d6afa2eb0618c32770ac3a23
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53865160"
---
# <a name="idebugengine3loadsymbols"></a>IDebugEngine3::LoadSymbols
Yükleri (gerekirse) Bu hata ayıklama altyapısında hata ayıklaması yapılan tüm modüller için sembolleri.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT LoadSymbols();  
```  
  
```csharp  
int LoadSymbols();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Yok.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu, bu hata ayıklama altyapısı tarafından başvurulan tüm modüller için hata ayıklama sembolleri yükler. Yalnızca bunlar zaten yüklü olan, semboller yüklenir. Simgeleri bir çağrı tarafından ayarlanmış olduğu yolları üzerinde aranır [SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md)   
 [IDebugEngine3](../../../extensibility/debugger/reference/idebugengine3.md)