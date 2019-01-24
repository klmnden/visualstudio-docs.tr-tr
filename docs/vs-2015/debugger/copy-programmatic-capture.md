---
title: Kopyalama (programlı yakalama) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 30ec235a-0abb-44b9-8852-61bc9e67ce22
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fa79ffc2081ba92b905838658fe6aa758a675192
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764682"
---
# <a name="copy-programmatic-capture"></a>Kopyalama (Programlı Yakalama)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Etkin bir grafik günlüğü (.vsglog) dosyasının içeriğini yeni bir dosyaya kopyalar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
void Copy(  
  wchar_t const * szNewVSGLog  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `szNewVSGLog`  
 Yeni grafik günlük dosyasının dosya adı.  
  
## <a name="remarks"></a>Açıklamalar  
 Grafik bilgilerini yeni bir dosya kopyalamak için zaten bazı grafik bilgilerini yakalanan gerekir; Aksi takdirde, hiçbir şey olmaz.
