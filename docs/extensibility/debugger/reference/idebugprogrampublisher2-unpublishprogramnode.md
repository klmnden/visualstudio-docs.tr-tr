---
title: IDebugProgramPublisher2::UnpublishProgramNode | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramPublisher2::UnpublishProgramNode
helpviewer_keywords:
- IDebugProgramPublisher2::UnpublishProgramNode
ms.assetid: 57c7e6e1-b84e-4e14-ad83-cbbb64e2f526
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 56eb23466d0364cbe22046bbb36be593a83a0998
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56698709"
---
# <a name="idebugprogrampublisher2unpublishprogramnode"></a>IDebugProgramPublisher2::UnpublishProgramNode
Belirtilen program düğüm altyapıları (DEs) ve oturum hata ayıklama Yöneticisi (SDM) hata ayıklamak için kullanıma sunulmasından kaldırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT UnpublishProgramNode(
   IDebugProgramNode2* pProgramNode
);
```

```csharp
int UnpublishProgramNode(
   IDebugProgramNode2 pProgramNode
);
```

#### <a name="parameters"></a>Parametreler
 `pProgramNode`

 [in] Bir [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) kaldırılmakta olan program düğümü temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Kaldırıldıktan sonra program düğümü artık program bilgilerinin konumu Sorgulanacak kullanılabilir değil.

 Bir program düğümü kullanılabilir hale getirmek için çağrı [PublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-publishprogramnode.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProgramPublisher2](../../../extensibility/debugger/reference/idebugprogrampublisher2.md)
- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
- [PublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-publishprogramnode.md)