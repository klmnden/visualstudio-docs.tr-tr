---
title: Iwefdebuggingsupport arabirimi
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
ms.openlocfilehash: a71adf5371275fbbdc19cdf09be96ef900ec073d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62583769"
---
# <a name="iwefdebuggingsupport-interface"></a>Iwefdebuggingsupport arabirimi
  Office uygulamalarında hata ayıklamayı kolaylaştırmak için Visual Studio'yu gibi bir hata ayıklama ortamı tarafından uygulanır. Word veya Excel gibi Office uygulamasını Visual Studio'dan bu arabirim alır ve ardından yöntemleri arabirimindeki bazı noktalarda hata ayıklama oturumu sırasında çağırır.

## <a name="syntax"></a>Sözdizimi

```csharp
[
    uuid(ccaf1a90-ce1c-4199-9cd6-b40c5c57a671),
    oleautomation
]
interface IWefDebuggingSupport : IUnknown
{
    HRESULT SetWefProcessId(
        [in] DWORD dwProcessId);
    HRESULT GetAutoInsertExtensions(
        [out, retval] SAFEARRAY(BSTR)* psaExtensionNames);
}
```

## <a name="methods"></a>Yöntemler
 Iwefdebuggingsupport arabirimi tanımlar yöntemler aşağıdaki tabloda listelenmiştir.

|Ad|Açıklama|
|----------|-----------------|
|[Getautoınsertextensions metodu](../vsto/getautoinsertextensions-method.md)|Hata ayıklama sırasında otomatik olarak eklenmesi için Office için uygulamalar hakkında bilgi alır.|
|[Setwefprocessıd yöntemi](../vsto/setwefprocessid-method.md)|Web uzantılarının Framework (WEF) içeriği çalışacak işlem tanımlayıcısı sağlar.|
