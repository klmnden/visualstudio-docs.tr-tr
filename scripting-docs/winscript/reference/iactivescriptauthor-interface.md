---
title: Iactivescriptauthor arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptAuthor interface
ms.assetid: df1f454d-01ee-4beb-928b-48513d07365a
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bd9d9c2a330ee72c6a843cd42586a09bb1d51e3c
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54346377"
---
# <a name="iactivescriptauthor-interface"></a>IActiveScriptAuthor Arabirimi
IntelliSense ve harmanlama bilgileri gibi hizmetler yazma temsil eder.  
  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IActiveScriptAuthor` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IActiveScriptAuthor::AddNamedItem](../../winscript/reference/iactivescriptauthor-addnameditem.md)|Komut dosyası altyapısının ad alanı yazma kök düzeyinde öğe adını ekler. A *kök düzeyinde öğe* özellikleri ve yöntemleri içerebilir ve bu de içerebilir bir olay kaynağı bir nesnedir.|  
|[IActiveScriptAuthor::AddScriptlet](../../winscript/reference/iactivescriptauthor-addscriptlet.md)|Kök düzeyinde alt sitesi olarak kod oluşturma yöntemini ekler `IScriptNode` nesne. Konak, yalnızca iki düzeyi ayrıldığında tam adı olabilir.|  
|[IActiveScriptAuthor::AddTypeLib](../../winscript/reference/iactivescriptauthor-addtypelib.md)|Komut dosyası için ad alanı için bir tür kitaplığı ekler.|  
|[IActiveScriptAuthor::GetChars](../../winscript/reference/iactivescriptauthor-getchars.md)|İstenen tamamlama bağlamı için tamamlama karakter kümesini döndürür.|  
|[IActiveScriptAuthor::GetEventHandler](../../winscript/reference/iactivescriptauthor-geteventhandler.md)|Belirtilen öznitelikleri scriptlet döndürür.|  
|[IActiveScriptAuthor::GetInfoFromContext](../../winscript/reference/iactivescriptauthor-getinfofromcontext.md)|Döndürür bir kod bloğu içinde bilgi ve belirli bir karakter için yer işareti konumlarını yazın. Bu üye için bilgi IntelliSense, genel listeler ve parametre ipuçları sağlar.|  
|[IActiveScriptAuthor::GetLanguageFlags](../../winscript/reference/iactivescriptauthor-getlanguageflags.md)|Dil bilgileri döndürür.|  
|[IActiveScriptAuthor::GetRoot](../../winscript/reference/iactivescriptauthor-getroot.md)|Döndürür `IScriptNode` yazarın betiği ağacının kökü.|  
|[IActiveScriptAuthor::GetScriptletTextAttributes](../../winscript/reference/iactivescriptauthor-getscriptlettextattributes.md)|Bir kod oluşturma metni özniteliklerini döndürür.|  
|[IActiveScriptAuthor::GetScriptTextAttributes](../../winscript/reference/iactivescriptauthor-getscripttextattributes.md)|Bir betik bloğu metin özniteliklerini döndürür.|  
|[IActiveScriptAuthor::IsCommitChar](../../winscript/reference/iactivescriptauthor-iscommitchar.md)|Belirli bir karakterin bir deyim tamamlama uygulama tarafından işleme olup olmadığını gösteren bir değer döndürür.|  
|[IActiveScriptAuthor::ParseScriptText](../../winscript/reference/iactivescriptauthor-parsescripttext.md)|Betik metin ayrıştırır, geliştirme komut dosyası altyapısı yazma metin ekler ve oluşturur bir `IScriptEntry` betik bloğu için karşılık gelen nesne.|  
|[IActiveScriptAuthor::RemoveNamedItem](../../winscript/reference/iactivescriptauthor-removenameditem.md)|Kaldırır bir `NamedItem` altyapısı yazma betiğin ad alanından nesne.|  
|[IActiveScriptAuthor::RemoveTypeLib](../../winscript/reference/iactivescriptauthor-removetypelib.md)|Bir tür kitaplığı altyapısı ad alanı yazma komut dosyasından kaldırır.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Yazma Arabirimleri](../../winscript/reference/active-script-authoring-interfaces.md)