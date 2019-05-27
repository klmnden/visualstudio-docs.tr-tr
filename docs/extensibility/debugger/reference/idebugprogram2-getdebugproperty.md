---
title: IDebugProgram2::GetDebugProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::GetDebugProperty
helpviewer_keywords:
- IDebugProgram2::GetDebugProperty
ms.assetid: d194224e-f0e6-46ab-85d4-9e2639e28946
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 660d8f40b2a9d3ead0010c1139a3d887d0524aa9
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212321"
---
# <a name="idebugprogram2getdebugproperty"></a>IDebugProgram2::GetDebugProperty
Programın özelliklerini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetDebugProperty( 
   IDebugProperty2** ppProperty
);
```

```csharp
int GetDebugProperty( 
   out IDebugProperty2 ppProperty
);
```

## <a name="parameters"></a>Parametreler
`ppProperty`\
[out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) programın özellikleri temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem tarafından döndürülen programa özgü özelliklerdir. Program birden fazla özelliği döndürme gerekiyorsa sonra [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) bu yöntem tarafından döndürülen nesne ek özellikleri ve arama bir kapsayıcıdır [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md) yöntemi döndürür bir tüm özelliklerin listesi.

 Bir program herhangi sayısı ve türü ile açıklanan ek özellikler getirebilir `IDebugProperty2` arabirimi. Bir IDE ek program özelliklerinin genel özellik tarayıcı kullanıcı arabirimi aracılığıyla görüntülenebilir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md)