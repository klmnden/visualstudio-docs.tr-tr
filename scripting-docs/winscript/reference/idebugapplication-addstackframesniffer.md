---
title: IDebugApplication::AddStackFrameSniffer | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.AddStackFrameSniffer
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::AddStackFrameSniffer
ms.assetid: a7a9684a-14c5-415a-ae63-a17397d58d07
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 16fb941a91482c548284dc3d4317a472fd9be641
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62991056"
---
# <a name="idebugapplicationaddstackframesniffer"></a>IDebugApplication::AddStackFrameSniffer
Bu uygulama için bir yığın çerçevesi Numaralandırıcı sağlayıcısı ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddStackFrameSniffer(  
   IDebugStackFrameSniffer*  pdsfs,  
   DWORD*                    pdwCookie  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdsfs`  
 [in] Bu uygulama eklemek için yığın çerçeve Numaralandırıcı sağlayıcısı.  
  
 `pdwCookie`  
 [out] Bu yığın çerçevesi Numaralandırıcı sağlayıcı uygulamayı kaldırmak için kullanılan tanımlama bilgisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Dil altyapıları genellikle yığın çerçevelerine hata ayıklayıcı kullanıma sunmak için bu yöntemi çağırın, bu yığın çerçevesi ortaya çıkarmak diğer varlıklar için mümkündür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md)   
 [IDebugApplication::RemoveStackFrameSniffer](../../winscript/reference/idebugapplication-removestackframesniffer.md)   
 [IDebugStackFrameSniffer Arabirimi](../../winscript/reference/idebugstackframesniffer-interface.md)