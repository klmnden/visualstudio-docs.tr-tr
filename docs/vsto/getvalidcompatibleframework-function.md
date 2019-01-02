---
title: GetValidCompatibleFramework işlevi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 30a116993535e3b99b4e91edf07752c00a020859
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53835493"
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
