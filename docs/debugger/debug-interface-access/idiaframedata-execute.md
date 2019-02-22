---
title: Idiaframedata::Execute | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::execute method
ms.assetid: 7a6c7d03-1ff1-4059-bd54-5f407eeebc26
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 78440c703ece2aa54e54594d57156dbb17848915
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56617710"
---
# <a name="idiaframedataexecute"></a>IDiaFrameData::execute
Yığın geriye doğru izleme gerçekleştirir ve sonuçları yığın ilerlemesi çerçeve arabiriminde döndürür.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT execute ( 
   IDiaStackWalkFrame* frame
);
```

#### <a name="parameters"></a>Parametreler
 `frame`

[in] Bir [Idiastackwalkframe](../../debugger/debug-interface-access/idiastackwalkframe.md) çerçeve yazmaçların durumu tutan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Aşağıdaki tabloda, bu yöntem olası dönüş değerleri gösterir.

|Değer|Açıklama|
|-----------|-----------------|
|E_DIA_INPROLOG|Giriş kodundaki yığın çerçevesi yürütülemiyor.|
|E_DIA_SYNTAX|Ayrıştırma hatası çerçeve programında karşılaşıldı.|
|E_DIA_FRAME_ACCESS|Erişim kayıtları veya bellek alınamıyor.|
|E_DIA_VALUE|Bir değerin (örneğin, sıfıra bölünme) hesaplama hatası.|

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, yığın geriye doğru izleme hata ayıklama sırasında çağrılır. [Idiastackwalkframe](../../debugger/debug-interface-access/idiastackwalkframe.md) nesne kayıtlar için güncelleştirmeleri almak ve tarafından kullanılan yöntemleri sağlaması için istemci uygulaması tarafından gerçekleştirilir `execute` yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)
- [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md)