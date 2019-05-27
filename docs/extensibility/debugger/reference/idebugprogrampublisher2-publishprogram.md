---
title: IDebugProgramPublisher2::PublishProgram | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramPublisher2::PublishProgram
helpviewer_keywords:
- IDebugProgramPublisher2::PublishProgram
ms.assetid: 92ff63f0-e869-4040-b3ae-b2c899e708ff
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: fb2fc0da42bf3895f6eefac96441dde2fa6eede9
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66203715"
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