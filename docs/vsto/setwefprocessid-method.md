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
ms.openlocfilehash: 1352ccc9318061be4a2f9ad2da7d63715acd6721
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56603086"
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
