---
title: IEEVisualizerServiceProvider::CreateVisualizerService | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEVisualizerServiceProvider::CreateVisualizerService
helpviewer_keywords:
- IEEVisualizerServiceProvider::CreateVisualizerService method
ms.assetid: f366f7c9-358d-46c8-993f-32ff86539833
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 20a8180283e596eeb9dd4ee1391e6e8fe6666829
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66310168"
---
# <a name="ieevisualizerserviceprovidercreatevisualizerservice"></a>IEEVisualizerServiceProvider::CreateVisualizerService
Bu yöntem Görselleştirici hizmeti oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CreateVisualizerService(
   IDebugBinder*              binder,
   IDebugSymbolProvider*      pSymProv,
   IDebugAddress*             pAddress,
   IEEVisualizerDataProvider* dataProvider,
   IEEVisualizerService**     ppService
);
```

```csharp
int CreateVisualizerService(
   IDebugBinder binder,
   IDebugSymbolProvider      pSymProv,
   IDebugAddress             pAddress,
   IEEVisualizerDataProvider dataProvider,
   out IEEVisualizerService  ppService
);
```

## <a name="parameters"></a>Parametreler
`binder`\
[in] [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) geçirilen nesne [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md).

`pSymProv`\
[in] [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md) geçirilen nesne `IDebugParsedExpression::EvaluateSync`.

`pAddress`\
[in] [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) geçirilen nesne `IDebugParsedExression::EvaluateSync`.

`dataProvider`\
[in] Bir nesneyi uygulama [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md) arabirimi (ifade değerlendiricisi tarafından sağlanan).

`ppService`\
[out] Oluşturulan hizmet.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 `binder`, `pSymProv`, Ve `pAddress` parametreler tüm gönderildi `IDebugParsedExpression::EvaluateSync` yöntemi. `CreateVisualizerService` yalnızca öğesinden çağrılması için `IDebugParsedExpression::EvaluateSync` tür görselleştiricileri desteği ifade değerlendiricisi'nın bir parçası olarak.

## <a name="see-also"></a>Ayrıca bkz.
- [IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)
- [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)
- [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)