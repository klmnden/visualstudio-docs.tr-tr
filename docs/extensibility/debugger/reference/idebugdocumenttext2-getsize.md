---
title: IDebugDocumentText2::GetSize | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocumentText2::GetSize
helpviewer_keywords:
- IDebugDocumentText2::GetSize
ms.assetid: bf515a8f-dcee-4004-8f81-543d547ceaae
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4f9c46066393a930f6f30208940f0d18b3ed0883
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59665582"
---
# <a name="idebugdocumenttext2getsize"></a>IDebugDocumentText2::GetSize
Belgedeki bu konumda metin boyutunu alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSize( 
   ULONG* pcNumLines,
   ULONG* pcNumChars
);
```

```csharp
int GetSize( 
   ref uint pcNumLines,
   ref uint pcNumChars
);
```

#### <a name="parameters"></a>Parametreler
 `pcNumLines`

 [out] Metin satırlarını döndürür.

 `pcNumChars`

 [out] Metin karakter sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar

 [C++ yalnızca] Belirli bir değeri istenildiği gibi değilse, parametre için NULL geçirin.

 [C# yalnızca] Her iki parametre belirtilmelidir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugDocumentText2](../../../extensibility/debugger/reference/idebugdocumenttext2.md)