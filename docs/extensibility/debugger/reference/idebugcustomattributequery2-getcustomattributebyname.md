---
title: IDebugCustomAttributeQuery2::GetCustomAttributeByName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCustomAttributeQuery2::GetCustomAttributeByName
helpviewer_keywords:
- IDebugCustomAttributeQuery2::GetCustomAttributeByName
ms.assetid: 7428dfeb-8929-41b2-9b99-cb343a86c02d
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7d874a00c3c82108c224f18922f2b4853279beaa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66322208"
---
# <a name="idebugcustomattributequery2getcustomattributebyname"></a>IDebugCustomAttributeQuery2::GetCustomAttributeByName
Özel öznitelik adı verilen özel öznitelikler bayt sayısını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetCustomAttributeByName( 
   LPCOLESTR pszCustomAttributeName,
   BYTE*     ppBlob,
   DWORD*    pdwLen
);
```

```csharp
int GetCustomAttributeByName(
   [In] string        pszCustomAttributeName,
   [In, Out] byte[]   ppBlob,
   [In, Out] ref uint pdwLen
);
```

## <a name="parameters"></a>Parametreler
`pszCustomAttributeName`\
[in] Aranacak özel özniteliğin adını içeren bir dize.

`ppBlob`\
[out içinde] Özel öznitelik bayt ile doldurulmuş bir dizi.

`pdwLen`\
[out içinde] Bayt olarak döndürülecek en fazla sayısını belirtir `ppBlob` dizisi ve diziye gerçekte yazılan bayt sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür veya özel öznitelik yoksa, S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Ayarlama `ppBlob` kullanılabilir bayt sayısını döndürmek için bir null değer parametresi öznitelikleri. Ardından bir dizi ayırmak ve geçirmek için bu dizide `ppBlob` parametresi.

 Öznitelik bayt özel özniteliğinin ham verileri temsil eder.

 Varsa `ppBlob` ve `pdwLen` parametreleri null bir değere ayarlamak, bu yöntem, özel özniteliği yalnızca mevcut olup olmadığını belirlemek için kullanılabilir. Daha kolay bir alternatif, ancak çağırmaktır [IsCustomAttributeDefined](../../../extensibility/debugger/reference/idebugcustomattributequery2-iscustomattributedefined.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugCustomAttributeQuery2](../../../extensibility/debugger/reference/idebugcustomattributequery2.md)
- [IsCustomAttributeDefined](../../../extensibility/debugger/reference/idebugcustomattributequery2-iscustomattributedefined.md)