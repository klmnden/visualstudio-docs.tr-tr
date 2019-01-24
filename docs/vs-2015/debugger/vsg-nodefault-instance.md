---
title: VSG_NODEFAULT_INSTANCE | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 19c95b0d-9a4d-441f-9ed7-3acb39e67521
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 9c7d2263642c2ff8a2c36f274d2c7b80745ed845
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54757136"
---
# <a name="vsgnodefaultinstance"></a>VSG_NODEFAULT_INSTANCE
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Varsayılan örneği olup olmadığını, varlığı tanımlayan [VsgDbg sınıfı](../debugger/vsgdbg-class.md) sınıfı — programlı yakalama arabirimi sağlayan — sağlanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
#define VSG_NODEFAULT_INSTANCE  
```  
  
## <a name="value"></a>Değer  
 Bir önişlemci tarafından varlığını simgesini veya olmaması, varsayılan örneği olup olmadığını belirler `VsgDbg` sınıfı sağlanır. Bu simge tanımlanmazsa, ardından hiçbir varsayılan örneğini `VsgDbg` sınıfı sağlanır; Aksi takdirde, varsayılan bir örnek sağlanan ve programınızı çalıştırılmadan önce başlatılır.  
  
 Programlı yakalama arabirimi genel kapsamda olan bir işaretçi yoluyla sağlanır `g_pVsgDbg`.  
  
```  
VsgDbg *g_pVsgDbg;  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Varsayılan örnek genellikle yeterli olur, ancak bu DLL dışında D3D cihazı oluşturulduğunda programlı yakalama arabirim bir DLL içinde kullanmak için oluşturabilir ve kendi örneğini yönetme `VsgDbg` sınıfı. Bu şekilde programlı yakalama API için kendi arabirimi yönetiyorsanız tanımlayarak varsayılan örneği devre dışı `VSG_NODEFAULT_INSTANCE` ek yükten kaçınmak için.  
  
 Varsayılan örnek devre dışı değil ise, program çalışmadan önce otomatik olarak başlatılır ve programınızı sona erdiğinde otomatik olarak yok. Başlatma veya bu örneğin açıkça uninitialize gerekmez.  
  
 Varsayılan örnek devre dışı bırakmak için tanımlamalısınız `VSG_NODEFAULT_INSTANCE` dahil önce `vsgcapture.h` programınızdaki.  
  
## <a name="example"></a>Örnek  
 Bu örnek, varsayılan örnek devre dışı bırakma gösterir:  
  
```  
// Define VSG_NODEFAULT_INSTANCE before including vsgcapture.h  
#define VSG_NODEFAULT_INSTANCE  
  
#include <vsgcapture.h>  
```
