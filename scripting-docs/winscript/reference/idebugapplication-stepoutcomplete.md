---
title: IDebugApplication::StepOutComplete | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.StepOutComplete
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::StepOutComplete
ms.assetid: 9675b214-7be5-4cf7-a63f-7865f3c54371
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 04f8ecfb835199afa0a60f3fde3c8fbdc8812240
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62990611"
---
# <a name="idebugapplicationstepoutcomplete"></a>IDebugApplication::StepOutComplete
İşlem Hata Ayıklama Yöneticisi tek adımlı modda bir dil altyapısı hakkında arayanına döndürülecek olduğunu bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT StepOutComplete();  
```  
  
#### <a name="parameters"></a>Parametreler  
 Bu yöntem parametre almaz.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Kendi çağırana döndürmeleri önce dil altyapıları tek adımlı modda bu yöntemi çağırın. İşlem Hata Ayıklama Yöneticisi bu fırsattan ilk fırsatta sonu diğer tüm komut dosyası motorları bildirmek için kullanır. Bu teknik, modları uygulanır nasıl diller arası adımdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplication Arabirimi](../../winscript/reference/idebugapplication-interface.md)