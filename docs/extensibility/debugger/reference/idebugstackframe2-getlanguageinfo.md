---
title: IDebugStackFrame2::GetLanguageInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugStackFrame2::GetLanguageInfo
helpviewer_keywords:
- IDebugStackFrame2::GetLanguageInfo
ms.assetid: 0e12fd92-f155-46a7-8272-cda279388cfb
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 90fd7beabb14163558afe4b957d95635e91f904a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56719554"
---
# <a name="idebugstackframe2getlanguageinfo"></a>IDebugStackFrame2::GetLanguageInfo
Bu yığın çerçevesiyle ilgili dilini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetLanguageInfo ( 
   BSTR* pbstrLanguage,
   GUID* pguidLanguage
);
```

```csharp
int GetLanguageInfo ( 
   ref string pbstrLanguage,
   ref Guid   pguidLanguage
);
```

#### <a name="parameters"></a>Parametreler
 `pbstrLanguage`

 [out] Bu yığın çerçevesiyle ilgili yöntemini uygulayan dil adını döndürür.

 `pguidLanguage`

 [out] Döndürür `GUID` dili. İçin [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] diller, örneğin, aşağıdaki döndürülen:

-   `guidVBScriptLang`

-   `guidJScriptLang`

-   `guidCPPLang`

-   `guidVBLang`

-   `guidSQLLang`

-   `guidScriptLang`

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)