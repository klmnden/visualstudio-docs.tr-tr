---
title: IDispError::GetSource | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDispError.GetSource
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDispError::GetSource
ms.assetid: 20def54c-a67c-4102-babf-6f0704e5fc5c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6f793675d40c87e4c64c2a83d37327f5222d8d1f
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144894"
---
# <a name="idisperrorgetsource"></a>IDispError::GetSource
Sınıf veya hataya neden olan uygulama için dile bağlı programlı tanımlayıcı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetSource(  
   BSTR*  pbstrSource  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrSource`  
 [out] Biçiminde bir programlı tanımlayıcı içeren dize `progname.objectname`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, özel durumun oluştuğu sınıf veya uygulamayı belirlemek için kullanılır. Program tanımlayıcısı çağırma sırasındaki sağlanan yerel ayar tanıtıcısı (LCID) tarafından belirtilen dilde döndürülebilir.  
  
> [!NOTE]
>  Bu yöntem uygulanmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDispError Arabirimi](../../winscript/reference/idisperror-interface.md)