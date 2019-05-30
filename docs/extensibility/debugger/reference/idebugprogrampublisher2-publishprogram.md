---
title: IDebugProgramPublisher2::PublishProgram | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramPublisher2::PublishProgram
helpviewer_keywords:
- IDebugProgramPublisher2::PublishProgram
ms.assetid: 92ff63f0-e869-4040-b3ae-b2c899e708ff
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 5d4f0b279bafe5291679237efdaada7907ddc515
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66343364"
---
# <a name="idebugprogrampublisher2publishprogram"></a>IDebugProgramPublisher2::PublishProgram
Bu yöntem, bir program hata ayıklama altyapısı (DEs) için kullanılabilir ve oturum hata ayıklama Yöneticisi sağlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT PublishProgram(
   CONST_GUID_ARRAY Engines,
   LPCOLESTR        szFriendlyName,
   IUnknown*        pDebuggeeInterface
);
```

```csharp
int PublishProgram(
   CONST_GUID_ARRAY Engines,
   string           szFriendlyName,
   object           pDebuggeeInterface
);
```

## <a name="parameters"></a>Parametreler
`Engines`\
[in] Başlatabilir veya bu programa ekleme GUID'ler DEs için bir dizi.

`szFriendlyName`\
[in] (Bu Bu menüler ya da iletişim kutuları kullanıcıya görünür) programı için kolay ad.

`pDebuggeeInterface`\
[in] `IUnknown` programı arabirimi (Bu değer bir tanımlama bilgisi program benzersiz olarak tanımlanabilmesi için kullanılır; bu değer "program yayımdan kaldırmak için" kullanılır)

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir programı hata ayıklama için artık kullanılabilir hale getirmek için çağrı [UnpublishProgram](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogram.md).

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProgramPublisher2](../../../extensibility/debugger/reference/idebugprogrampublisher2.md)
- [UnpublishProgram](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogram.md)