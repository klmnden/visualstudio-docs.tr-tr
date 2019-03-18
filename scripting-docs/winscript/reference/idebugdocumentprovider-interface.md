---
title: Idebugdocumentprovider arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentProvider interface
ms.assetid: 36510acf-1ef9-479c-a430-d3f09502f82c
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5632134c86b5aa0e3cb769a68d2d4cfd944ff35c
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157216"
---
# <a name="idebugdocumentprovider-interface"></a>IDebugDocumentProvider Arabirimi
İsteğe bağlı bir belge oluşturmak için gereken araçları sağlar.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir belge örnekleme için dolaylı anlamına gelir:  
  
- Gerektiğinde yüklenecek belge sağlar.  
  
- IDE hata ayıklayıcısı içinde dahil edilmek üzere belge nesnesi sağlar.  
  
- Aynı belge nesneye erişmek için birden çok yol sağlar.  
  
  Bu etkin belgeyi kendi sağlayıcısından ayırır ve ek çalışma zamanı bağlam bilgilerini taşımak sağlayıcı sağlar.  
  
  Devralınan yöntemleri yanı sıra `IDebugDocumentInfo`, `IDebugDocumentProvider` arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugDocumentProvider::GetDocument](../../winscript/reference/idebugdocumentprovider-getdocument.md)|Zaten yoksa, oluşturulacak belge neden olur.|