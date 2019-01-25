---
title: GetValidCompatibleFramework işlevi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 79b97867a3a5c87f1e208d93efacea711ba71efc
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54869313"
---
# <a name="getvalidcompatibleframework-function"></a>GetValidCompatibleFramework işlevi
  Bu API Office altyapısını destekler ve doğrudan kodunuzdan kullanılmaya yönelik değildir.  

## <a name="syntax"></a>Sözdizimi  

```csharp 
HRESULT WINAPI GetValidCompatibleFramework(  
    LPCWSTR lpwszCompatibleFrameworksXML,  
    BSTR* pbstrValidFrameworkTag  
);  
```  

### <a name="parameters"></a>Parametreler  

|Parametre|Açıklama|  
|---------------|-----------------|  
|*lpwszCompatibleFrameworksXML*|Kullanmayın.|  
|*pbstrValidFrameworkTag*|Kullanmayın.|  

## <a name="return-value"></a>Dönüş değeri  
 İşlev başarılı olursa, döndürür **S_OK**. İşlev başarısız olursa hata kodu döndürür.  
