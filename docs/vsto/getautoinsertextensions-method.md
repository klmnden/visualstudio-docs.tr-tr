---
title: Getautoınsertextensions metodu
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 9716f6adcee1d443e342074f3c46a57a1ace26db
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53915896"
---
# <a name="getautoinsertextensions-method"></a>Getautoınsertextensions metodu
  Hata ayıklama sırasında otomatik olarak eklenmesi için Office için uygulamalar hakkında bilgi alır.  
  
 Bu yöntem, gelecekte kullanılmak üzere ayrılmıştır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```csharp
HRESULT GetAutoInsertExtensions(  
    [out, retval] SAFEARRAY(BSTR)* psaExtensionNames  
);  
```  
  
### <a name="parameters"></a>Parametreler  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|*psaExtensionNames*|Office için uygulamalar uzantı adları.|  
  
## <a name="return-value"></a>Dönüş değeri  
 Yöntemi başarıyla tamamlanıp tamamlanmadığını belirten bir HRESULT değer.  
  
## <a name="remarks"></a>Açıklamalar  
 Her uygulama için eklenecek Office altındaki bir değere karşılık gelen bir Office uygulaması uzantı adı olarak döndürülen **HKEY_CURRENT_USER\Software\Microsoft\Office\WEF\Developer**. Konak, bu kayıt defteri değerlerini arayın ve uzantılar otomatik olarak ekler.  
