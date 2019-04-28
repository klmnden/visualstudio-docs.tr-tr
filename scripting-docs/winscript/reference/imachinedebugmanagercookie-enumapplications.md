---
title: IMachineDebugManagerCookie::EnumApplications | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IMachineDebugManagerCookie.EnumApplications
apilocation:
- scrobj.dll
helpviewer_keywords:
- IMachineDebugManagerCookie::EnumApplications
ms.assetid: 03f863cf-fa7f-4ec4-b1a1-1ae0ad296c39
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 76d8e53d586a812f4a8416a1515d7011dd5a1720
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977623"
---
# <a name="imachinedebugmanagercookieenumapplications"></a>IMachineDebugManagerCookie::EnumApplications
Çalışan uygulamalar geçerli listenin bir numaralandırıcı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnumApplications(  
   IEnumRemoteDebugApplications**  ppeda  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppeda`  
 [out] Geçerli çalışan uygulamaların listesini içeren bir numaralandırıcı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, çalışan uygulamaların geçerli listenin bir numaralandırıcı döndürür. Hata ayıklayıcı IDE görüntülemek ve hata ayıklama amacıyla uygulamalar eklemek için bu yöntemi kullanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IMachineDebugManagerCookie Arabirimi](../../winscript/reference/imachinedebugmanagercookie-interface.md)