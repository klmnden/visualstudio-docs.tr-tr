---
title: Idiasession::findınjectedsource | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findInjectedSource method
ms.assetid: 907531b6-1ef8-4153-986d-b72611a1632d
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 11a4134ce02ca540cdffff9cc51a1280bd4173bf
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752239"
---
# <a name="idiasessionfindinjectedsource"></a>IDiaSession::findInjectedSource
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Öznitelik sağlayıcıları tarafından sembol deposuna yerleştirilen kaynaklarının listesi veya diğer bileşenleri derleme işleminin alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT findInjectedSource (   
   LPCOLESTR                 srcFile,  
   IDiaEnumInjectedSources** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 Trgblob  
 [in] Aranmak üzere kaynak dosyasının adı.  
  
 ppResult  
 [out] Döndürür bir [Idiaenumınjectedsources](../../debugger/debug-interface-access/idiaenuminjectedsources.md) tüm eklenen kaynakları listesini içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumınjectedsources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)   
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
