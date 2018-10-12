---
title: IDiaSession::findAcceleratorInlineesByName | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
ms.assetid: e203e5c2-6563-43fa-be56-3063955043ab
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: dec89bc2259be8d4f940b52134abf938954ea73f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49273305"
---
# <a name="idiasessionfindacceleratorinlineesbyname"></a>IDiaSession::findAcceleratorInlineesByName
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirtilen satır içi işlev adına karşılık gelen satır içi çerçeveler için semboller numaralandırmasını döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT findAcceleratorInlineeLinesByName (   
   LPCOLESTR             name,  
   DWORD                 option,  
   IDiaEnumSymbols**     ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `name`  
 [in] Aranacak toplandığı için satır içi işlev adı.  
  
 `option`  
 [in] Çerçeveler için satır içi arama yapılırken kullanılacak adı arama seçeneklerini karşılık `name`. Daha fazla bilgi için [NameSearchOptions numaralandırması](../../debugger/debug-interface-access/namesearchoptions.md).  
  
 `ppResult`  
 [out] Bir işaretçi bir `IDiaEnumSymbols` sonucu ile başlatılmış bir arabirim işaretçisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu işlev yalnızca içinde Hızlandırıcı saplama işlevleri inlinees arar. Yerel C++ yordamı kayıtları yoksayar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiaenumsymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



