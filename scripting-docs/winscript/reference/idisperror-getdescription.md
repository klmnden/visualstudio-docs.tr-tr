---
title: IDispError::GetDescription | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispError.GetDescription
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDispError::GetDescription
ms.assetid: 04deaea6-0265-4e34-952e-634edba0e923
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5505113ee650c6618be5a95bc77244daf90cfcb7
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63446955"
---
# <a name="idisperrorgetdescription"></a>IDispError::GetDescription
Hata metinsel açıklaması döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetDescription(  
   BSTR*  pbstrDescription  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrDescription`  
 [out] Hata kısa bir açıklamasını içeren dize.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Metin için geçirilen yerel ayar tanıtıcısı (LCID) tarafından belirtilen dilde döndürülür `IDispatchEx::InvokeEx` hatayla yöntemi.  
  
> [!NOTE]
> Bu yöntem uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idisperror arabirimi](../../winscript/reference/idisperror-interface.md)   
 [IDispatchEx::InvokeEx](../../winscript/reference/idispatchex-invokeex.md)