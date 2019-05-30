---
title: IDebugProcess2::CanDetach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess2::CanDetach
helpviewer_keywords:
- IDebugProcess2::CanDetach
ms.assetid: 2830f7c3-69fb-474a-97b8-5b869e38d546
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 83cb927d86604096eac89da1d0efdf7e64e209be
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353220"
---
# <a name="idebugprocess2candetach"></a>IDebugProcess2::CanDetach
Oturum hata ayıklama Yöneticisi (SDM) bir işlem ayırabilirsiniz belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CanDetach(
   void
);
```

```csharp
int CanDetach();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK.` döndürür `S_FALSE` hata ayıklayıcı işlemden ayırma yapılamıyor. Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [CanDetach](../../../extensibility/debugger/reference/idebugprogram2-candetach.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)