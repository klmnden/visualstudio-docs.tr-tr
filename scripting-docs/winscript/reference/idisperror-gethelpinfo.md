---
title: IDispError::GetHelpInfo | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispError.GetHelpInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDispError::GetHelpInfo
ms.assetid: a146df13-eda4-4e56-8bf0-cf9886a2150f
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fa831ff511ea507e03ca858b93383ff38ead9039
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63446915"
---
# <a name="idisperrorgethelpinfo"></a>IDispError::GetHelpInfo
Yardım dosyasının yolu ve mümkünse, hatayı açıklayan bir konu bağlam Kimliğini döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetHelpInfo(  
   BSTR*  pbstrFileName,  
   DWORD*  pdwContext  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrFileName`  
 [out] Yardım dosyasının tam yolu içeren dize. Yardım dosyası yok veya bir hata oluşursa, döndürülen değer NULL olur.  
  
 `pdwContext`  
 [out] Hata için Yardım içeriği kimliği. Yardım dosyası yoksa (varsa `pbstrFileName` null), bu parametre bir anlamı yoktur.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_FAIL`|Sağlayıcıya özgü bir hata oluştu.|  
|`E_INVALIDARG`|`pbstrFileName` veya `pdwContext` NULL idi.|  
|`E_OUTOFMEMORY`|Sağlayıcı, Yardım dosyası yol döndürmek yeterli bellek ayıramadı.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, Yardım dosyasının yolu ve mümkünse, hatayı açıklayan bir konu bağlam Kimliğini döndürür.  
  
> [!NOTE]
> Bu yöntem uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDispError Arabirimi](../../winscript/reference/idisperror-interface.md)