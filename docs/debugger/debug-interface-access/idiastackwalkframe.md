---
title: Idiastackwalkframe | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkFrame interface
ms.assetid: 42d82845-d6f6-4846-9ecd-9dd169216077
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 343c56e3d3175c26900b0cfb4cdc3d816a324404
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56630593"
---
# <a name="idiastackwalkframe"></a>IDiaStackWalkFrame
Yığın bağlamı çağrıları arasında tutar [Idiaframedata::Execute](../../debugger/debug-interface-access/idiaframedata-execute.md) yöntemi.

## <a name="syntax"></a>Sözdizimi

```
IDiaStackWalkFrame : IUnknown
```

## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDiaStackWalkFrame`.

|Yöntem|Açıklama|
|------------|-----------------|
|[IDiaStackWalkFrame::get_registerValue](../../debugger/debug-interface-access/idiastackwalkframe-get-registervalue.md)|Bir kayıt değeri alır.|
|[IDiaStackWalkFrame::put_registerValue](../../debugger/debug-interface-access/idiastackwalkframe-put-registervalue.md)|Bir kayıt değeri ayarlar.|
|[IDiaStackWalkFrame::readMemory](../../debugger/debug-interface-access/idiastackwalkframe-readmemory.md)|Bellek görüntüden okur.|
|[IDiaStackWalkFrame::searchForReturnAddress](../../debugger/debug-interface-access/idiastackwalkframe-searchforreturnaddress.md)|Belirtilen yığın çerçevesinin yakın işlevi dönüş adresi arar.|
|[IDiaStackWalkFrame::searchForReturnAddressStart](../../debugger/debug-interface-access/idiastackwalkframe-searchforreturnaddressstart.md)|Belirtilen yığın çerçevesinin veya belirtilen adres'e yakın bir dönüş adresi arar.|

## <a name="remarks"></a>Açıklamalar
 Bu arabirim, program yürütme sırasında okuma ve yazma kayıtlarını yanı sıra bellek erişim ve dönüş adresi bulmak için kullanılır.

## <a name="notes-for-callers"></a>Arayanlar İçin Notlar
 İstemci uygulaması bu arabirimi uygulayan ve bir arabirimin örneğini geçirir [Idiaframedata::Execute](../../debugger/debug-interface-access/idiaframedata-execute.md) yöntemi. Bu arabirim'ın aynı örneğine tekrar tekrar her çağrılması sırasında kasalar durumunu korumak için kullanılır `execute` yöntemi. `execute` Yöntemi de bu arabirimi dönüş adresi belirlemek için kullanır.

## <a name="requirements"></a>Gereksinimler
 Üst bilgi: dia2.h

 Kitaplık: diaguids.lib

 DLL: msdia80.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Arabirimler (Arabirim Erişimi SDK'sında Hata Ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaFrameData::execute](../../debugger/debug-interface-access/idiaframedata-execute.md)