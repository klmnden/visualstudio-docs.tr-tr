---
title: Idialoadcallback2 | Microsoft Docs
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
helpviewer_keywords:
- IDiaLoadCallback2 interface
ms.assetid: 9a44277d-cbed-4811-9bad-5a2aa0f09323
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 06ddc1a27dceafb2b526925f6ee6649b1d62c6ff
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49180303"
---
# <a name="idialoadcallback2"></a>IDiaLoadCallback2
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Yordam bulma, bulmayla işlemi uygulanan için kısıtlamaları izin vererek DIA Sembol'nden geri çağırmaları alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDiaLoadCallback2 : IDiaLoadCallback  
```  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemlere ek olarak [Idialoadcallback](../../debugger/debug-interface-access/idialoadcallback.md) arabirimi bu arabirim, aşağıdaki yöntemi kullanıma sunar:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDiaLoadCallback2::RestrictOriginalPathAccess](../../debugger/debug-interface-access/idialoadcallback2-restrictoriginalpathaccess.md)|Özgün hata ayıklama dizinindeki bir .pdb dosyasını arayan belirler.|  
|[IDiaLoadCallback2::RestrictReferencePathAccess](../../debugger/debug-interface-access/idialoadcallback2-restrictreferencepathaccess.md)|.Exe dosyasının bulunduğu yolu bir .pdb dosyasını ararken izin verilip verilmediğini belirler.|  
|[IDiaLoadCallback2::RestrictDBGAccess](../../debugger/debug-interface-access/idialoadcallback2-restrictdbgaccess.md)|Hata ayıklama ile ilgili bilgi arayan .dbg dosyaları izin verilip verilmediğini belirler.|  
|[IDiaLoadCallback2::RestrictSystemRootAccess](../../debugger/debug-interface-access/idialoadcallback2-restrictsystemrootaccess.md)|Sistem kök dizininde .pdb dosyalarını aramaya izin verilip verilmediğini belirler.|  
  
## <a name="remarks"></a>Açıklamalar  
 İstemci uygulaması bu arabirimi uygulayan ve çağrısında ona başvuru sağlayan [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md) yöntemi. Tüm yöntemlere uygulanacağını unutmayın [Idialoadcallback](../../debugger/debug-interface-access/idialoadcallback.md) de arabirimi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: Dia2.h  
  
 Kitaplık: diaguids.lib  
  
 DLL: msdia80.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Arabirimler (arabirim erişimi SDK'SINDA hata ayıklama)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [Idiadatasource::loaddataforexe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)   
 [Idiareadexeatoffsetcallback](../../debugger/debug-interface-access/idiareadexeatoffsetcallback.md)   
 [Idiareadexeatrvacallback](../../debugger/debug-interface-access/idiareadexeatrvacallback.md)   
 [IDiaLoadCallback](../../debugger/debug-interface-access/idialoadcallback.md)



