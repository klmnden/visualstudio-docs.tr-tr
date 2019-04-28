---
title: IDebugStackFrameSnifferEx::EnumStackFramesEx | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugStackFrameSnifferEx.EnumStackFramesEx
apilocation:
- jscript.dll
helpviewer_keywords:
- IDebugStackFrameSnifferEx::EnumStackFramesEx
ms.assetid: b656b581-aff0-4984-8d8a-a1c7a8e6558a
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8969c279e4eb2c2966e297317a25a60f12be68a9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63005725"
---
# <a name="idebugstackframesnifferexenumstackframesex"></a>IDebugStackFrameSnifferEx::EnumStackFramesEx
Geçerli iş parçacığı için yığın çerçevelerinin bir numaralandırıcı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnumStackFramesEx(  
   DWORD_PTR                dwSpMin,  
   IEnumDebugStackFrames**  ppedsf  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwSpMin`  
 [in] Yığın çerçevelerini numaralandırma alt adresi sınırı.  
  
 `ppedsf`  
 [out] Geçerli iş parçacığı için yığın çerçevesi için Numaralandırıcı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yığın çerçeve Numaralandırıcı çerçeveleri ile en son gönderilen çerçevenin yığın üstüne başlayarak döndürür. Numaralandırıcı yalnızca büyük veya eşittir adresleriyle yığın çerçeveleri içeriyor `dwSpMin`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugStackFrameSnifferEx Arabirimi](../../winscript/reference/idebugstackframesnifferex-interface.md)