---
title: Başlatmış | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 4cd4fc0b-974a-4e61-9ea8-0aaa1a0c52ea
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 48c4e76105c024f9f414a884c2e3cabde716db86
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55019115"
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