---
title: İleti numaralandırıcısı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- message enumerator
- source control plug-ins, message enumeration
ms.assetid: 4a4faa0d-d352-40ea-a21d-c09ea286a8e1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 37932ce6e64361692d659355e9ab6e88ee5462ed
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62806505"
---
# <a name="message-enumerator"></a>İleti numaralandırıcısı
Aşağıdaki bayrakları için kullanılan `TEXTOUTPROC` işlevini çağırdığında, IDE sağlayan bir geri çağırma işlevidir [SccOpenProject](../extensibility/sccopenproject-function.md) (bkz [LPTEXTOUTPROC](../extensibility/lptextoutproc.md) geri çağırma hakkında ayrıntılı bilgi için işlevi).

 İşlemi iptal etmek için IDE istenirse, iptal iletilerinden birini alabilirsiniz. Bu durumda, kaynak denetim eklentisini kullanan `SCC_MSG_STARTCANCEL` görüntülemek için IDE sormak **iptal** düğmesi. Bundan sonra herhangi bir dizi normal ileti gönderilebilir. Bu döndürür varsa `SCC_MSG_RTN_CANCEL`, eklenti işlemi çıkar ve döndürür. Ayrıca eklentinin yoklar `SCC_MSG_DOCANCEL` düzenli aralıklarla kullanıcı işlemi iptal etti belirlemek için. Tüm işlemler yapılır ya da devre dışı kullanıcı iptal etti, eklenti gönderirken `SCC_MSG_STOPCANCEL`. `SCC_MSG_INFO`, SCC_MSG_WARNING, ve SCC_MSG_ERROR türleri, iletileri kaydırma listesinde gösterilen iletileri için kullanılır. `SCC_MSG_STATUS` metin bir durum çubuğu veya geçici görüntüleme alanı içinde gösterilmesi gerekir olduğunu gösteren özel bir türdür. Kalıcı olarak listede kalmaz.

## <a name="syntax"></a>Sözdizimi

```
enum { 
   SCC_MSG_RTN_CANCEL = -1, 
   SCC_MSG_RTN_OK = 0, 
   SCC_MSG_INFO = 1 
   SCC_MSG_WARNING, 
   SCC_MSG_ERROR, 
   SCC_MSG_STATUS, 
   SCC_MSG_DOCANCEL, 
   SCC_MSG_STARTCANCEL, 
   SCC_MSG_STOPCANCEL 
};
```

## <a name="members"></a>Üyeler
 SCC_MSG_RTN_CANCEL iptal belirtmek için gelen geri dönün.

 SCC_MSG_RTN_OK iade den devam etmek için geri çağırma.

 SCC_MSG_INFO ileti bilgilendirme amaçlıdır.

 SCC_MSG_WARNING ileti bir uyarıdır.

 SCC_MSG_ERROR, bir hata iletisidir.

 SCC_MSG_STATUS ileti durum çubuğu için tasarlanmıştır.

 Metin SCC_MSG_DOCANCEL yok; IDE döndürür `SCC_MSG_RTN_OK` veya `SCC_MSG_RTN_CANCEL`.

 SCC_MSG_STARTCANCEL başlar iptal bir döngü.

 SCC_MSG_STOPCANCEL iptal döngü durdurur.

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak denetimi eklentileri](../extensibility/source-control-plug-ins.md)
- [LPTEXTOUTPROC](../extensibility/lptextoutproc.md)