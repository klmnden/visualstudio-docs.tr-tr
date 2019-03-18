---
title: IActiveScript::AddTypeLib | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScript.AddTypeLib
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScript_AddTypeLib
ms.assetid: 8e507ea8-c80a-471c-b482-ae753c6e8595
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c4943d1305c2f25de4eec9e782949a66827de879
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144881"
---
# <a name="iactivescriptaddtypelib"></a>IActiveScript::AddTypeLib
Komut dosyası için ad alanı için bir tür kitaplığı ekler. Bu benzer `#include` C/C++'ta yönergesi. Sınıf tanımları gibi önceden tanımlanmış öğelerin kümesi sağlayan `typedefs`ve komut dosyası çalışma zamanı ortamına eklenecek sabitleri adlı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddTypeLib(  
    REFGUID guidTypeLib,  // CLSID of type library  
    DWORD dwMaj,          // major version number  
    DWORD dwMin,          // minor version number  
    DWORD dwFlags         // option flags  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guidTypeLib`  
 [in] Eklenecek CLSID tür kitaplığının.  
  
 `dwMaj`  
 [in] Ana sürüm numarası.  
  
 `dwMin`  
 [in] İkincil sürüm numarası.  
  
 `dwFlags`  
 [in] Seçeneğini işaretler. Aşağıdakiler olabilir:  
  
|Değer|Açıklama|  
|-----------|-------------|  
|SCRIPTTYPELIB_ISCONTROL|Ana bilgisayar tarafından kullanılan bir ActiveX denetimi tür kitaplığını açıklar.|  
  
## <a name="return-value"></a>Dönüş Değeri  
 Aşağıdaki değerlerden birini döndürür:  
  
|Dönüş Değeri|Açıklama|  
|------------------|-------------|  
|`S_OK`|Başarılı.|  
|`E_INVALIDARG`|Bir bağımsız değişken geçersiz.|  
|`E_UNEXPECTED`|Çağrı beklenmiyordu (örneğin, komut dosyası altyapısı henüz yüklenen başlatıldı veya).|  
|`TYPE_E_CANTLOADLIBRARY`|Belirtilen tür kitaplığı yüklenemedi.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScript](../../winscript/reference/iactivescript.md)