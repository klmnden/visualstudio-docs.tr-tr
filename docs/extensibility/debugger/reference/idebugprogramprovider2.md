---
title: IDebugProgramProvider2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramProvider2
helpviewer_keywords:
- IDebugProgramProvider2 interface
ms.assetid: a9ec7b3e-a59c-4069-b2ee-6f45916eeb78
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2789601c6fd3c10fe1fa11609eaadb7febbd26c1
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457753"
---
# <a name="idebugprogramprovider2"></a>IDebugProgramProvider2
Bu kayıtlı arabirim Yöneticisi (SDM) "aracılığıyla yayımlanan" programlar hakkında bilgi edinmek için oturum hata ayıklama sağlayan [IDebugProgramPublisher2](../../../extensibility/debugger/reference/idebugprogrampublisher2.md) arabirimi.

## <a name="syntax"></a>Sözdizimi

```
IDebugProgramProvider2 : IUnknown
```

## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar
Hata ayıklama altyapısı (DE), ayıklanan programlar hakkında bilgi sağlamak için bu arabirimi uygular. Bu arabirim ölçüm kullanarak kayıt defterini DE bölümünde kayıtlı `metricProgramProvider`anlatılan şekilde [hata ayıklama için SDK Yardımcıları](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md).

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
COM'ın arama `CoCreateInstance` işleviyle `CLSID` kayıt defterinden alınan program sağlayıcısı. Örneğe bakın.

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri

|Yöntem|Açıklama|
|------------|-----------------|
|[GetProviderProcessData](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md)|Çalışan, çeşitli yollarla filtrelenmiş programlar hakkında bilgi edinir.|
|[GetProviderProgramNode](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprogramnode.md)|Bir program düğümü verilen bir özel işlem kimliği alır.|
|[WatchForProviderEvents](../../../extensibility/debugger/reference/idebugprogramprovider2-watchforproviderevents.md)|Belirli türde işlemleri ile ilişkili sağlayıcı olayları izlemek üzere bir geri çağırma oluşturur.|
|[SetLocale](../../../extensibility/debugger/reference/idebugprogramprovider2-setlocale.md)|Bir yerel ayar için DE tarafından gereken tüm dile özgü kaynakları oluşturur.|

## <a name="remarks"></a>Açıklamalar
Normalde, bir işlem, bu işlemde çalışan programlar hakkında bilgi edinmek için bu arabirimi kullanır.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="example"></a>Örnek

```cpp
IDebugProgramProvider2 *GetProgramProvider(GUID *pDebugEngineGuid)
{
    // This is typically defined globally. For this example, it is
    // defined here.
    static const WCHAR strRegistrationRoot[] = L"Software\\Microsoft\\VisualStudio\\8.0Exp";
    IDebugProgramProvider2 *pProvider = NULL;
    if (pDebugEngineGuid != NULL) {
        CLSID clsidProvider = { 0 };
        ::GetMetric(NULL,
                    metrictypeEngine,
                    *pDebugEngineGuid,
                    metricProgramProvider,
                    &clsidProvider,
                    strRegistrationRoot);
        if (!IsEqualGUID(clsidProvider,GUID_NULL)) {
            CComPtr<IDebugProgramProvider2> spProgramProvider;
            spProgramProvider.CoCreateInstance(clsidProvider);
            if (spProgramProvider != NULL) {
                pProvider = spProgramProvider.Detach();
            }
        }
    }
    return(pProvider);
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [Temel Arabirimler](../../../extensibility/debugger/reference/core-interfaces.md)
- [IDebugProgramPublisher2](../../../extensibility/debugger/reference/idebugprogrampublisher2.md)
- [Hata Ayıklama için SDK Yardımcıları](../../../extensibility/debugger/reference/sdk-helpers-for-debugging.md)
