---
title: IDebugExpressionContext2::GetName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugExpressionContext2::GetName
helpviewer_keywords:
- IDebugExpressionContext2::GetName
ms.assetid: c2b70d22-17af-4986-a7e3-930910367216
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 20004fd424bbb394c4c6d0a80df94d408e86285c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56706528"
---
# <a name="idebugexpressioncontext2getname"></a>IDebugExpressionContext2::GetName
Değerlendirme bağlamı adını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetName( 
   BSTR* pbstrName
);
```

```csharp
int GetName( 
   out string pbstrName
);
```

#### <a name="parameters"></a>Parametreler
 `pbstrName`

 [out] Değerlendirme bağlamı adını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu değerlendirme bağlamı açıklamasını addır. Bu genellikle bu tam değerlendirme içeriğe başvuruda bulunan bir ifade değerlendiricisi tarafından ayrıştırılan bir şeydir. Örneğin, c++'ta adı aşağıdaki gibidir:

```
"{ function-name, source-file-name, module-file-name }"
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md)