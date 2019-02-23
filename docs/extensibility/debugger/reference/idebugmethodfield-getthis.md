---
title: IDebugMethodField::GetThis | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMethodField::GetThis
helpviewer_keywords:
- IDebugMethodField::GetThis method
ms.assetid: cc235bea-e909-4d8c-ab54-936736c803fc
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8fc3c4a37b30d2ce7d4f5228b60d6c411afb5c9f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56700555"
---
# <a name="idebugmethodfieldgetthis"></a>IDebugMethodField::GetThis
Alır `this` (`Me` içinde [!INCLUDE[vbprvb](../../../code-quality/includes/vbprvb_md.md)]) metodunu içeren nesne işaretçisi.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetThis( 
   IDebugClassField** ppClass
);
```

```csharp
int GetThis(
   out IDebugClassField ppClass
);
```

#### <a name="parameters"></a>Parametreler
 `ppClass`

 [out] Döndürür bir [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md) "Bu" işaretçiyi temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Nesne yönelimli dillerde, genellikle geçerli bir sınıf örneğinin örtülü bir işaretçi yok. Bu olarak bilinir `this` C# / C++ ve `Me` içinde [!INCLUDE[vbprvb](../../../code-quality/includes/vbprvb_md.md)].

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)
- [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)