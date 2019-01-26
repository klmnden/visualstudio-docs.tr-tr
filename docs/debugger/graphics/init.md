---
title: Init | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c55ddec8-9101-4673-979b-4109caca9146
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 61c3d580c4e9e0362629d70c23e0b918fe698429
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54983462"
---
# <a name="init"></a>Init
Etkin bir şekilde yakalayıp grafik bilgilerini bir grafik günlük dosyasına kaydetmek için grafik tanılama uygulama bileşeninin hazırlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
void Init(  
  std::function<void (int len, wchar_t * pszBuffer)> vsgLogGetter  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `vsgLogGetter`  
 Aranabilir bir varlık — işlevi, işlev işaretçisi, lambda veya işlev nesnesi gibi — oluşan bir arabellek uzunluğu parametre olarak alan `wchar_t` ve bir işaretçi, arabellek ve döndürür `void`. Çağrıldığında çağrılabilir varlık grafik bilgilerini kaydetmek için kullanılır ve sonuç döndürülmeden önce belirtilen arabelleğe Yazar dosya adını belirler.  
  
## <a name="remarks"></a>Açıklamalar  
 `Init` İşlevi örneği otomatik olarak çağrılır `VsgDbg` sınıfı belirterek yapılandırılmıştır `bDefaultInit` parametre, oluşturucunun `true`; Aksi takdirde `Init` açıkça önce çağrılmalıdır etkin bir şekilde yakalayabilir ve grafik bilgilerini kaydedin.  
  
 Sonlandırma ve Kapat etkin grafikler çağırarak günlük dosyası `UnInit`, ardından yakalama ve yeni bir grafik günlük dosyası için daha fazla grafik bilgisi çağırarak kayıt `Init` yeniden. Bu olarak aynı kullanarak günlük dosyalarını birden fazla bağımsız grafik oluşturmak istediğiniz kadar tekrarlayabilirsiniz `VsgDbg` örneği.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [UnInit](init.md)