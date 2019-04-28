---
title: Iactivescriptprofilercallback3::setwebworkerıd yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 47744746-1276-441e-ab60-2a78f550e8e2
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0798a23b4c8ad4e5859bec73ebfed47a56b322d6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62993109"
---
# <a name="iactivescriptprofilercallback3setwebworkerid-method"></a>IActiveScriptProfilerCallback3::SetWebWorkerId Yöntemi
Profil Oluşturucu bu profil oluşturma oturumu için kullanılacak alt kimliği hakkında bilgilendirir. İşlevi, sayfa bağlamında yürütülmüyor, bu yöntem çağrılır değil. Değerini `webWorkerId` 1'den başlayarak, her bir çalışan için 1 artar. Kimliği değerleri bir oturumu kararlı ve çalışanlar oluşturulduğu sırada yalnızca karşılık gelen kullanılmaya yönelik değildir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetWebWorkerId([in] DWORD webWorkerId);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `webWorkerId`  
 Web çalışanı kimliği  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntemin dönüş değerini komut dosyası altyapısı tarafından göz ardı edilir.