---
title: Getautoınsertextensions metodu
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
ms.openlocfilehash: fb767ec7301a1d4e0f29003971b017339228fc9f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62972284"
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
