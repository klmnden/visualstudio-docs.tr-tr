---
title: VSG_NODEFAULT_INSTANCE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 19c95b0d-9a4d-441f-9ed7-3acb39e67521
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 304576391b2287aee7567b3ccc2e4514ce5cb2e8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62848465"
---
# <a name="vsgnodefaultinstance"></a>VSG_NODEFAULT_INSTANCE
Varsayılan örneği olup olmadığını, varlığı tanımlayan [VsgDbg sınıfı](vsgdbg-class.md) sınıfı — programlı yakalama arabirimi sağlayan — sağlanır.

## <a name="syntax"></a>Sözdizimi

```C++
#define VSG_NODEFAULT_INSTANCE
```

## <a name="value"></a>Değer
 Bir önişlemci tarafından varlığını simgesini veya olmaması, varsayılan örneği olup olmadığını belirler `VsgDbg` sınıfı sağlanır. Bu simge tanımlanmazsa, ardından hiçbir varsayılan örneğini `VsgDbg` sınıfı sağlanır; Aksi takdirde, varsayılan bir örnek sağlanan ve programınızı çalıştırılmadan önce başlatılır.

 Programlı yakalama arabirimi genel kapsamda olan bir işaretçi yoluyla sağlanır `g_pVsgDbg`.

```cpp
VsgDbg *g_pVsgDbg;
```

## <a name="remarks"></a>Açıklamalar
 Varsayılan örnek genellikle yeterli olur, ancak bu DLL dışında D3D cihazı oluşturulduğunda programlı yakalama arabirim bir DLL içinde kullanmak için oluşturabilir ve kendi örneğini yönetme `VsgDbg` sınıfı. Bu şekilde programlı yakalama API için kendi arabirimi yönetiyorsanız tanımlayarak varsayılan örneği devre dışı `VSG_NODEFAULT_INSTANCE` ek yükten kaçınmak için.

 Varsayılan örnek devre dışı değil ise, program çalışmadan önce otomatik olarak başlatılır ve programınızı sona erdiğinde otomatik olarak yok. Başlatma veya bu örneğin açıkça uninitialize gerekmez.

 Varsayılan örnek devre dışı bırakmak için tanımlamalısınız `VSG_NODEFAULT_INSTANCE` dahil önce `vsgcapture.h` programınızdaki.

## <a name="example"></a>Örnek
 Bu örnek, varsayılan örnek devre dışı bırakma gösterir:

```cpp
// Define VSG_NODEFAULT_INSTANCE before including vsgcapture.h
#define VSG_NODEFAULT_INSTANCE

#include <vsgcapture.h>
```
