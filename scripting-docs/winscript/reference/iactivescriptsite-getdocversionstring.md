---
title: IActiveScriptSite::GetDocVersionString | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSite.GetDocVersionString
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSite_GetDocVersionString
ms.assetid: ab3f892d-06d3-4cb5-9ea5-20c4a1e518cd
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a451f4883373978772643e11fe22feb9122be30e
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097220"
---
# <a name="iactivescriptsitegetdocversionstring"></a>IActiveScriptSite::GetDocVersionString
Geçerli belge sürümü benzersiz olarak tanımlayan ve ana bilgisayar tanımlı bir dize alır. Komut dosyası altyapısı ilgili bir belge, Windows komut dosyası (Not Defteri ile düzenlenmekte olan bir HTML sayfası olduğu gibi) kapsamı dışında değiştiyse, bu betik bir sonraki yüklendiğinde çalışabilmeleri zorlama kalıcı durumunu birlikte kaydedebilirsiniz.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDocVersionString(  
    BSTR *pbstrVersionString  // address of document version string  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstrVersionString`  
 [out] Konak tarafından tanımlanan belge sürüm dizesi adresi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa veya `E_NOTIMPL` varsa, bu yöntem desteklenmiyor.  
  
## <a name="remarks"></a>Açıklamalar  
 Varsa `E_NOTIMPL` döndürülür, komut dosyası altyapısı betik belge ile eşitlenmiş olduğunu varsayın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md)