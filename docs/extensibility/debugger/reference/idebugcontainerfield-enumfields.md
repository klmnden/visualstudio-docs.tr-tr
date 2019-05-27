---
title: IDebugContainerField::EnumFields | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugContainerField::EnumFields
helpviewer_keywords:
- IDebugContainerField::EnumFields method
ms.assetid: 9e5e681b-ad49-4c62-bd95-4afa11d61a57
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 368b076f592cff44e95e7156265c049a143fe1a3
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66205822"
---
# <a name="idebugcontainerfieldenumfields"></a>IDebugContainerField::EnumFields
Kapsayıcının alanlar için bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumFields( 
   FIELD_KIND         dwKindFilter,
   FIELD_MODIFIERS    dwModifiersFilter,
   LPCOLESTR          pszNameFilter,
   NAME_MATCH         nameMatch,
   IEnumDebugFields** ppEnum
);
```

```csharp
int EnumFields(
   enum_ FIELD_KIND      dwKindFilter,
   enum_ FIELD_MODIFIERS dwModifiersFilter,
   string                pszNameFilter,
   NAME_MATCH            nameMatch,
   out IEnumDebugFields  ppEnum
);
```

## <a name="parameters"></a>Parametreler
`dwKindFilter`\
[in] Bir birleşimi [FIELD_KIND](../../../extensibility/debugger/reference/field-kind.md) sabitler sıralanması alanları seçin. Depolama türleri, örneğin sınıf ya da temel veya özel bilgiler, yerel, parametre veya "Bu" işaretçi gibi alan türlerini tanımlayabilirsiniz.

`dwModifiersFilter`\
[in] Bir birleşimi [FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md) sabitler sıralanması alanları seçin. Alan değiştiricilerini genel veya özel sanal, statik ya da son gibi depolama bilgilerini gibi erişim izinlerini olabilir.

`pszNameFilter`\
[in] Numaralandırılacak alanın adı. Tüm alanları döndürülecek ise bu null değeri olabilir.

`nameMatch`\
[in] Bir değer [NAME_MATCH](../../../extensibility/debugger/reference/name-match.md) veya arama olup olmadığını denetleyen sabit listesi duyarlıdır.

`ppEnum`\
[out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) alanların listesini temsil eden nesne. Alanı yoksa null değeri döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Alanı yoksa başarılıysa S_OK veya S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 `dwKindFilter`, `dwModifiersFilter`, Ve `pszNameFilter` parametreleri birleştirilebilir, örneğin, "MyMethod" adlı tüm genel sanal yöntemleri seçin.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)
- [FIELD_KIND](../../../extensibility/debugger/reference/field-kind.md)
- [FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md)
- [NAME_MATCH](../../../extensibility/debugger/reference/name-match.md)