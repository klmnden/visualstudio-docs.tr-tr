---
title: IActiveScript::GetScriptSite | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.GetScriptSite
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_GetScriptSite
ms.assetid: 83a2a89d-93d0-4cbd-9244-91a730cb406b
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b57c4282b7ec77eb4af2ffa983479ae77388e1c9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62935777"
---
# <a name="iactivescriptgetscriptsite"></a>IActiveScript::GetScriptSite
Windows komut dosyası motoruyla ilişkili site nesnesi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetScriptSite(  
    REFIID iid,           // interface identifier  
    void **ppvSiteObject  // address of host site interface  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `iid`  
 [in] İstenen arabirim tanımlayıcısı.  
  
 `ppvSiteObject`  
 [out] Ana bilgisayarın site nesnesi arabirim işaretçisi alır konumu adresi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_NOINTERFACE`|Belirtilen bir arabirim desteklenmiyor.|  
|`E_POINTER`|Geçersiz işaretçi belirtildi.|  
|`S_FALSE`|Site ayarlandı; `ppvSiteObject` parametrenin ayarlanmış `NULL`.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)