---
title: Setwefprocessıd yöntemi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 3ccce49992073f11245929bf7af0b966537bd079
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53886156"
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
