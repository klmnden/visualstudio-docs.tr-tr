---
title: Setwefprocessıd yöntemi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 7807d0495c5f0548178b1bc2ecae12d57cc3b072
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54876128"
---
# <a name="setwefprocessid-method"></a>Setwefprocessıd yöntemi
  Web uzantılarının Framework (WEF) içeriği çalışacak işlem tanımlayıcısı sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```csharp  
HRESULT SetWefProcessId(  
    [in] DWORD dwProcessId  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|*dwProcessId*|WEF içeriğini çalıştırmak için kullanılan işlem tanımlayıcısı.|  
  
## <a name="return-value"></a>Dönüş değeri  
 Yöntemi başarıyla tamamlanıp tamamlanmadığını belirten bir HRESULT değer.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, WEF içerik işlem oluşturulduktan sonra ancak herhangi bir WEF içerik çalışmadan önce çağrılmalıdır.  
  
 Geliştirme ortamını WEF içerik işleme hata ayıklayıcı iliştirmek istiyorsanız, ortam bu yöntemi uygulamanızda bu işlemi gerçekleştirmeniz gerekir.  
