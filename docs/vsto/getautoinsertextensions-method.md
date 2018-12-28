---
title: Getautoınsertextensions metodu
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: 9a12adf6e83e58b877e36dd65d98b617cda3a39b
ms.sourcegitcommit: a205ff1b389fba1803acd32c54df7feb0ef7a203
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53647216"
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
  
  