---
title: Init | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c55ddec8-9101-4673-979b-4109caca9146
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 06594b749b5d92781f6c3389ca6f5f9395c98c75
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53827253"
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