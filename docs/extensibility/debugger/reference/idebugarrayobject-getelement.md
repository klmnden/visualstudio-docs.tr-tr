---
title: IDebugArrayObject::GetElement | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugArrayObject::GetElement
helpviewer_keywords:
- IDebugArrayObject::GetElement method
ms.assetid: 08b44341-7bf1-4a8c-8b79-98ae5785b195
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 735b92bb649344c055f7a645b961925e3cbd4d6e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56684630"
---
# <a name="idebugarrayobjectgetelement"></a>IDebugArrayObject::GetElement
Bir dizideki öğe alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetElement( 
   DWORD          dwIndex,
   IDebugObject** ppElement
);
```

```csharp
int GetElement(
   [In] uint dwIndex,
   out IDebugObject ppElement
);
```

#### <a name="parameters"></a>Parametreler
 `dwIndex`

 [in] Öğenin dizini.

 `ppElement`

 [out] Döndürür bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) öğeyi temsil eden arabirim.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Çok boyutlu dizi nesnesi olsa bile, bu yöntem, bir dizi nesnesinin tüm öğeleri tek boyutlu dizi görür. Örneğin, bir dizi verilen `myarray[3][2][6]` ve `dwIndex` 20 parametresi, bu yöntem döndürmesine öğesinden `myarray[1][1][2]`ve bir `dwIndex` 21 parametresinin öğesinden döndürmesine `myarray[1][1][3]`. Kullanım [GetCount](../../../extensibility/debugger/reference/idebugarrayobject-getcount.md) dizideki öğelerin toplam sayısını belirlemek için yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md)