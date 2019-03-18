---
title: IActiveScriptParse::InitNew | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptParse.InitNew
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptParse_InitNew
ms.assetid: 3a582bd6-fc0d-43a5-812f-5ea55a8517a1
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 55d38031708694aa777f7598f261afdfc2b4f3b9
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58148954"
---
# <a name="iactivescriptparseinitnew"></a>IActiveScriptParse::InitNew
Komut dosyası altyapısı başlatır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT InitNew(void);  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa veya `E_FAIL` , başlatma sırasında bir hata oluştu.  
  
## <a name="remarks"></a>Açıklamalar  
 Komut dosyası altyapısı kullanılmadan önce aşağıdaki yöntemlerden birini çağrılmalıdır: `IPersist*::Load`, `IPersist*::InitNew`, veya `IActiveScriptParse::InitNew`. Bu yöntem semantiği özdeş `IPersistStreamInit::InitNew`bu yöntem kendisine başlatmak için komut dosyası altyapısı söyler. Bu. Her ikisi de çağırmak için geçerli olmadığını göz önünde bulundurun `IPersist*::InitNew` veya `IActiveScriptParse::InitNew` ve `IPersist*::Load`, veya çağırmak için geçerli değil `IPersist*::InitNew`, `IActiveScriptParse::InitNew`, veya `IPersist*::Load` birden çok kez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptParse](../../winscript/reference/iactivescriptparse.md)