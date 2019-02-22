---
title: IDiaSession::findAcceleratorInlineesByName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: e203e5c2-6563-43fa-be56-3063955043ab
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fb3caa5574605864a0dd16b59b6f451530b8e631
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56632244"
---
# <a name="idiasessionfindacceleratorinlineesbyname"></a>IDiaSession::findAcceleratorInlineesByName
Belirtilen satır içi işlev adına karşılık gelen satır içi çerçeveler için semboller numaralandırmasını döndürür.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT findAcceleratorInlineeLinesByName ( 
   LPCOLESTR             name,
   DWORD                 option,
   IDiaEnumSymbols**     ppResult
);
```

#### <a name="parameters"></a>Parametreler
 `name`

[in] Aranacak toplandığı için satır içi işlev adı.

 `option`

[in] Çerçeveler için satır içi arama yapılırken kullanılacak adı arama seçeneklerini karşılık `name`. Daha fazla bilgi için [NameSearchOptions numaralandırması](../../debugger/debug-interface-access/namesearchoptions.md).

 `ppResult`

[out] Bir işaretçi bir `IDiaEnumSymbols` sonucu ile başlatılmış bir arabirim işaretçisi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu işlev yalnızca içinde Hızlandırıcı saplama işlevleri inlinees arar. Yerel C++ yordamı kayıtları yoksayar.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)