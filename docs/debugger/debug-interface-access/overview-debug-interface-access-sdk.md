---
title: (Hata ayıklama arabirimi Erişim SDK'sı) genel bakış | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- user-defined types
- .dbg files
- modules
- interfaces [DIA SDK]
- DBG files
- procedures [DIA SDK]
- executable files
- COM objects, in DIA SDK
- compilands
- executable images
ms.assetid: 720b4479-a8bc-4fec-860e-80c1a0780405
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f159dcc58a096033516fdd272819b9eb1ad916d1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54922667"
---
# <a name="overview-debug-interface-access-sdk"></a>Genel Bakış (Arabirim Erişimi SDK'sında Hata Ayıklama)
DIA SDK'sı Microsoft hata ayıklama bilgilerine erişmek için kullanın. DIA SDK'sı bir COM tabanlı Microsoft hata ayıklama bilgileri biçimi değiştiğinde kodunuzu yeniden yazma gereğini ortadan kaldırıyor API kümesi sağlar. DIA SDK Ayrıca, bir grup önceki sürümleri tarafından oluşturulan .pdb ve .dbg dosyaları bulunan hata ayıklama bilgilerini okumak sağlar [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] 5.0 ve üzeri sürümler.  
  
 Her arabirimi DIA SDK içinde farklı bir COM nesnesi dışında başka türlü nerede temsil eder. Ek arabirimleri ve bu nedenle ek nesneler, oluşturulma açık sorguları yoluyla gibi [Idiadatasource::opensession](../../debugger/debug-interface-access/idiadatasource-opensession.md) veya [Idiasession::findchildren](../../debugger/debug-interface-access/idiasession-findchildren.md), yerine çağırarak`QueryInterface` üzerinde varolan arabirim işaretçileri.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiadatasource::opensession](../../debugger/debug-interface-access/idiadatasource-opensession.md)   
 [IDiaSession::findChildren](../../debugger/debug-interface-access/idiasession-findchildren.md)