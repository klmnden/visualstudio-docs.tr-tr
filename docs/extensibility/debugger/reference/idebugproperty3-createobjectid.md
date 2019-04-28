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
ms.openlocfilehash: cf17196b4dae8642a81664dd339eaa78c2d2d8e9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63412741"
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
> Her benzersiz kimliklerini istediği DE yapabilirsiniz, bu benzersiz kimliği almak için bir yöntem zaman `CreateObjectID` yöntemi çağrılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)
- [DestroyObjectID](../../../extensibility/debugger/reference/idebugproperty3-destroyobjectid.md)