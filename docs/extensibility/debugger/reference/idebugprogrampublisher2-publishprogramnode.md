---
title: IDebugProgramPublisher2::PublishProgramNode | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramPublisher2::PublishProgramNode
helpviewer_keywords:
- IDebugProgramPublisher2::PublishProgramNode
ms.assetid: d4b72e04-f726-46cf-8e56-5203ff205b12
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: e1b0611b723b649fd8d899af427c6b41fb5db1e1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66343291"
---
# <a name="idebugprogrampublisher2publishprogramnode"></a>IDebugProgramPublisher2::PublishProgramNode
Bir program düğüm hata ayıklama Yöneticisi (SDM) hata ayıklama altyapısı (DEs) kullanımına ve oturumu için kullanılabilir hale getirir.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT PublishProgramNode(
   IDebugProgramNode2 *pProgramNode
);
```

```csharp
int PublishProgramNode(
   IDebugProgramNode2 pProgramNode
);
```

## <a name="parameters"></a>Parametreler
`pProgramNode`\
[in] Bir [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) kullanılabilir hale getirmek için programı düğümünü temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem seçme ve hata ayıklama için başlatmadan önce bilgi sorgulanmasını olanak verir.

 Kullanılabilirlik bir program düğüm kaldırmak için çağrı [UnpublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogramnode.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgramPublisher2](../../../extensibility/debugger/reference/idebugprogrampublisher2.md)
- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
- [UnpublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogramnode.md)