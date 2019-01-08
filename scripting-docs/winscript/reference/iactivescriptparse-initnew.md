---
title: IActiveScriptParse::InitNew | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: f0998bea50d7839f93111aa6b116934fae35bfa3
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54089992"
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