---
title: Init | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: c55ddec8-9101-4673-979b-4109caca9146
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ea9f8a24d342668b3574c3798a32c58c124aca7b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54781757"
---
# <a name="init"></a>Init
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Etkin bir şekilde yakalayıp grafik bilgilerini bir grafik günlük dosyasına kaydetmek için grafik tanılama uygulama bileşeninin hazırlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
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
 [UnInit](../debugger/init.md)
