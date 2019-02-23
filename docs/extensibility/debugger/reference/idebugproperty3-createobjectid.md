---
title: IDebugProperty3::CreateObjectID | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProperty3::CreateObjectID
helpviewer_keywords:
- IDebugProperty3::CreateObjectID
ms.assetid: f2fa81e7-822f-456e-8729-a96a18eea771
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a523dd7886e46cf1df7c6e70024a052f62ca4748
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56694926"
---
# <a name="idebugproperty3createobjectid"></a>IDebugProperty3::CreateObjectID
Diğer özellikler arasında benzersiz olduğundan emin olmak için bu özellik için benzersiz bir kimliği oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CreateObjectID(
   void
);
```

```csharp
int CreateObjectID();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu özellik, diğer özellikler arasında benzersiz olarak tanımlanıyorsa emin olmak oturum hata ayıklama Yöneticisi istediğinde, bu yöntem çağrılır. Özellikleri ile ilgilenir zaten benzersiz şekilde tanımlanır sürece bu yöntemi hata ayıklama altyapısı (DE) destekler. DE bu metodu desteklemiyor varsa, döndürür `E_NOTIMPL`.

 Herhangi bir benzersiz kimliği ile oluşturulan `CreateObjectID` zaman yok [DestroyObjectID](../../../extensibility/debugger/reference/idebugproperty3-destroyobjectid.md) yöntemi çağrılır; bu da bu özellik benzersiz olarak tanımlamak için gereken sonuna işaret eder.

> [!NOTE]
>  Her benzersiz kimliklerini istediği DE yapabilirsiniz, bu benzersiz kimliği almak için bir yöntem zaman `CreateObjectID` yöntemi çağrılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)
- [DestroyObjectID](../../../extensibility/debugger/reference/idebugproperty3-destroyobjectid.md)