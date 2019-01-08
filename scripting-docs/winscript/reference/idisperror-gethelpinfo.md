---
title: IDispError::GetHelpInfo | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 8c2c8ae3a3cff2485c50901bb94ced83098e6000
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54087496"
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
>  Bu yöntem uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDispError Arabirimi](../../winscript/reference/idisperror-interface.md)