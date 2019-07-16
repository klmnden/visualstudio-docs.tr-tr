---
title: Başlatmış | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 4cd4fc0b-974a-4e61-9ea8-0aaa1a0c52ea
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0bec86a7f872057b7a0d652df6346e3a1ef2ff8a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68197932"
---
# <a name="uninit"></a>UnInit
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Grafik günlük dosyasını sonlandırır kapatılır ve uygulama, etkin bir şekilde grafik bilgilerini kaydetme sırasında kullanılan kaynakları serbest bırakır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
void UnInit();  
```  
  
## <a name="remarks"></a>Açıklamalar  
 `UnInit` örneği otomatik olarak çağrılır `VsgDbg` sınıfı yok edildiğinde. Varsa `VsgDbg` örneği etkin bir şekilde kaydetmediğiniz grafik bilgilerini, bu etkiye sahip değildir.  
  
 Sonra `UnInit` örneği üzerinde çağrıldıktan `VsgDbg` sınıfının yeni bir grafik günlük dosyasını çağırarak oluşturulabilir `Init` ve çağrı sonlandırılır `UnInit`. Bu kadar çok kez aynı kullanmak istediğiniz gibi yineleyebilirsiniz `VsgDbg` çeşitli bağımsız grafik günlük dosyaları oluşturmak için örneği.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Init](../debugger/init.md)
