---
title: IDebugProcessEx2::AddImplicitProgramNodes | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcessEx2::AddImplicitProgramNodes
helpviewer_keywords:
- IDebugProcessEx2::AddImplicitProgramNodes method
ms.assetid: 8b491b00-f9e7-45b3-9115-fe58c3464289
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b75ef50107b44de8de6f65c5c4c9c6827e13426e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309494"
---
# <a name="idebugprocessex2addimplicitprogramnodes"></a>IDebugProcessEx2::AddImplicitProgramNodes
Bu yöntem, belirtilen her hata ayıklama altyapısı (DE) için bir program düğüm ekler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT AddImplicitProgramNodes(
   REFGUID guidLaunchingEngine,
   GUID*   rgguidSpecificEngines,
   DWORD   celtSpecificEngines
);
```

```csharp
int AddImplicitProgramNodes(
   ref Guid guidLaunchingEngine,
   Guid[]   rgguidSpecificEngines,
   uint     celtSpecificEngines
);
```

## <a name="parameters"></a>Parametreler
`guidLaunchingEngine`\
[in] `GUID` , Program başlatmak için kullanılacak olan (ve kendi program düğümleri eklemek için kabul edilir) bir DE.

`rgguidSpecificEngines`\
[in] Dizi `GUID`DEs hangi programın düğümleri eklenir, s.

`celtSpecificEngines`\
[in] Sayısını `GUID`s'te `rgguidSpecificEngines` dizisi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
- [Program düğümleri](../../../extensibility/debugger/program-nodes.md) her DE listelenen için eklenecek `rgguidSpecificEngines`— başlatma altyapısı hariç (belirtildiği `guidLaunchingEngine`), bir program başlattığında kendi program düğümü eklemek için kabul.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgramEx2](../../../extensibility/debugger/reference/idebugprogramex2.md)
- [Program Düğümleri](../../../extensibility/debugger/program-nodes.md)