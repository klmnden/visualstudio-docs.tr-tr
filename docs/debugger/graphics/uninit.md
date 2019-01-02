---
title: Başlatmış | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 4cd4fc0b-974a-4e61-9ea8-0aaa1a0c52ea
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a1cb7898042ef7f6974d2ac43ca8630232edddfc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53884934"
---
# <a name="uninit"></a>UnInit
Grafik günlük dosyasını sonlandırır kapatılır ve uygulama, etkin bir şekilde grafik bilgilerini kaydetme sırasında kullanılan kaynakları serbest bırakır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
void UnInit();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 `UnInit` örneği otomatik olarak çağrılır `VsgDbg` sınıfı yok edildiğinde. Varsa `VsgDbg` örneği etkin bir şekilde kaydetmediğiniz grafik bilgilerini, bu etkiye sahip değildir.  
  
 Sonra `UnInit` örneği üzerinde çağrıldıktan `VsgDbg` sınıfının yeni bir grafik günlük dosyasını çağırarak oluşturulabilir `Init` ve çağrı sonlandırılır `UnInit`. Bu kadar çok kez aynı kullanmak istediğiniz gibi yineleyebilirsiniz `VsgDbg` çeşitli bağımsız grafik günlük dosyaları oluşturmak için örneği.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Init](init.md)