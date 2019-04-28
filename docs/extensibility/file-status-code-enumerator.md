---
title: Dosya durumu kod numaralandırıcısı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- named constants, SccStatus enumerator
- source control plug-ins, file status enumeration
- SccStatus enumerator
- file status code enumerator
ms.assetid: 5c37876b-c83c-4ca1-837b-57cd465a879a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 50312caddf0ce2b5c64d1ec83e1707e2e0ee086e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62863070"
---
# <a name="file-status-code-enumerator"></a>Dosya durumu kod numaralandırıcısı
`SccStatus` Numaralandırıcı kaynak denetimi sisteminizden bir dosya durumunu belirten adlandırılmış sabit değerleri içerir. Bu sabit listesi tarafından kullanılan [Sccqueryınfo](../extensibility/sccqueryinfo-function.md) ve `POPLISTFUNC` geri çağırma işlevi (bkz [POPLISTFUNC](../extensibility/poplistfunc.md) Ayrıntılar için).

## <a name="syntax"></a>Sözdizimi

```
enum SccStatus {
   SCC_STATUS_INVALID          = -1L,
   SCC_STATUS_NOTCONTROLLED    = 0x0000L,
   SCC_STATUS_CONTROLLED       = 0x0001L,
   SCC_STATUS_CHECKEDOUT       = 0x0002L,
   SCC_STATUS_OUTOTHER         = 0x0004L,
   SCC_STATUS_OUTEXCLUSIVE     = 0x0008L,
   SCC_STATUS_OUTMULTIPLE      = 0x0010L,
   SCC_STATUS_OUTOFDATE        = 0x0020L,
   SCC_STATUS_DELETED          = 0x0040L,
   SCC_STATUS_LOCKED           = 0x0080L,
   SCC_STATUS_MERGED           = 0x0100L,
   SCC_STATUS_SHARED           = 0x0200L,
   SCC_STATUS_PINNED           = 0x0400L,
   SCC_STATUS_MODIFIED         = 0x0800L,
   SCC_STATUS_OUTBYUSER        = 0x1000L
   SCC_STATUS_NOMERGE          = 0x2000L
   SCC_STATUS_RESERVED_1       = 0x4000L
   SCC_STATUS_RESERVED_2       = 0x8000L
};
```

## <a name="members"></a>Üyeler
 SCC_STATUS_INVALID durumu alınamadı; üzerinde güvenmeyin.

 SCC_STATUS_NOTCONTROLLED dosya kaynak denetimi altında değil.

 Kaynak denetimi altında SCC_STATUS_CONTROLLED dosyasıdır.

 SCC_STATUS_CHECKEDOUT iade out yerel diskte geçerli bir kullanıcı tarafından.

 SCC_STATUS_OUTOTHER dosya başka bir kullanıcı tarafından kullanıma alındı.

 SCC_STATUS_OUTEXCLUSIVE dosya özel olarak kullanıma.

 SCC_STATUS_OUTMULTIPLE dosya birden fazla kullanıcı tarafından kullanıma alındı.

 SCC_STATUS_OUTOFDATE dosyanın en son değil.

 Projeden SCC_STATUS_DELETED dosya silindi.

 SCC_STATUS_LOCKED dosyası kilitli; Daha fazla sürüm izin verilir.

 SCC_STATUS_MERGED dosya birleştirilmiş ancak henüz sabit/doğrulandı.

 SCC_STATUS_SHARED dosya projeler arasında paylaşılır.

 Açık bir sürüme paylaşılan SCC_STATUS_PINNED dosya.

 SCC_STATUS_MODIFIED dosya değiştirildiğinde/ayrılmış/ihlal olmuştur.

 SCC_STATUS_OUTBYUSER dosya geçerli bir kullanıcı tarafından kullanıma alındı.

 SCC_STATUS_NOMERGE dosya hiçbir zaman ile birleştirilebilir ve GET önce kaydedilmemiş.

 Ayrılmış SCC_STATUS_RESERVED_1 iç kullanım için.

 Ayrılmış SCC_STATUS_RESERVED_2 iç kullanım için.

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak denetimi eklentileri](../extensibility/source-control-plug-ins.md)
- [SccQueryInfo](../extensibility/sccqueryinfo-function.md)
- [POPLISTFUNC](../extensibility/poplistfunc.md)