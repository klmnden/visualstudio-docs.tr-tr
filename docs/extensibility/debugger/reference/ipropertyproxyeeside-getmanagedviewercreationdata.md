---
title: IPropertyProxyEESide::GetManagedViewerCreationData | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IPropertyProxyEESide::GetManagedViewerCreationData
helpviewer_keywords:
- IPropertyProxyEESide::GetManagedViewerCreationData
ms.assetid: c4eb4d60-8816-4d52-bc8d-dffd4f066499
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 435f6924948ab1273abbded633bcce757b57d9b3
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66329506"
---
# <a name="ipropertyproxyeesidegetmanagedviewercreationdata"></a>IPropertyProxyEESide::GetManagedViewerCreationData
Bu Görüntüleyici bir örneğini oluşturmak için bu özellik türü Görüntüleyicisi hakkında bilgi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetManagedViewerCreationData(
   BSTR*                  assemName,
   IEEDataStorage**       assemBytes,
   IEEDataStorage**       assemPdb,
   BSTR*                  className,
   ASSEMBLYLOCRESOLUTION* alr,
   BOOL*                  replacementOk
);
```

```csharp
int GetManagedViewerCreationData(
   out string                     assemName,
   out IEEDataStorage             assemBytes,
   out IEEDataStorage             assemPdb,
   out string                     className,
   out enum_ASSEMBLYLOCRESOLUTION alr,
   out int                        replacementOk
);
```

## <a name="parameters"></a>Parametreler
`assemName`\
[out] Bu nesne bulunduran derlemenin adını döndürür.

`assemBytes`\
[out] Döndürür bir [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) (Bu, bir null değer yok bayt mevcutsa) bu nesnenin derleme baytları içeren nesne.

`assemPdb`\
[out] Döndürür bir `IEEDataStorage` sembolü içeren bir nesne, bu nesne için (Bu, bir null değer hiçbir sembol deposu varsa) bilgileri depolar.

`className`\
[out] Bu nesneyi içeren sınıf adını döndürür.

`alr`\
[out] Bir değer döndürür [ASSEMBLYLOCRESOLUTION](../../../extensibility/debugger/reference/assemblylocresolution.md) derleme konumunu belirten sabit listesi.

`replacementOk`\
[out] Sıfır olmayan döndürür (`TRUE`) bu nesnenin değeri değiştirilebilir; sıfır (`FALSE`) nesne salt okunur ise.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, tür görselleştiricilerde, yönetilen bir Görüntüleyici örneklemek için kullanılır.

## <a name="see-also"></a>Ayrıca bkz.
- [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)
- [ASSEMBLYLOCRESOLUTION](../../../extensibility/debugger/reference/assemblylocresolution.md)
- [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)