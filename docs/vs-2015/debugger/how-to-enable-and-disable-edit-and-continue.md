---
title: 'Nasıl yapılır: Etkinleştirme ve devre dışı Düzenle ve devam et | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- /INCREMENTAL linker option
- Apply Code Changes command
- Edit and Continue, disabling
- code changes, applying in break mode
- INCREMENTAL linker option
- Edit and Continue, enabling
- break mode, applying code changes
- Edit and Continue, applying code changes
- Step command
- Go command
ms.assetid: fd961a1c-76fa-420d-ad8f-c1a6c003b0db
caps.latest.revision: 29
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 70914da9be4046589a0ca3b8e5fd4ae13210ca51
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65689257"
---
# <a name="how-to-enable-and-disable-edit-and-continue"></a>Nasıl yapılır: Etkinleştirme ve devre dışı Düzenle ve devam et
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Düzenle ve devam et, etkinleştirmek veya devre dışı **seçenekleri** tasarım zamanında iletişim kutusu. Hata ayıklarken bu ayarı değiştiremezsiniz.  
  
 Düzenle ve works yalnızca hata ayıklama yapılarında devam edin. Yerel C++ için Düzenle ve devam et gerektirir / Incremental kullanma seçeneği.  
  
## <a name="procedures"></a>Yordamlar  
  
#### <a name="to-enabledisable-edit-and-continue"></a>Etkinleştirmek/devre dışı Düzenle ve devam et  
  
1. Hata ayıklama seçenekleri sayfasını aç (**Araçlar / Seçenekler / hata ayıklama**).  
  
2. Ekranı aşağı kaydırarak **Düzenle ve devam et** kategorisi.  
  
3. Etkinleştirmek için seçin **etkinleştirme Düzenle ve devam et** onay kutusu. Devre dışı bırakmak için onay kutusunu temizleyin.  
  
   > [!NOTE]
   > Etkin IntelliTrace ve hem IntelliTrace olayları ve çağrı bilgilerini toplamak, Düzenle ve Devam Et'i devre dışı bırakılmıştır. Daha fazla bilgi için [yapılandırma IntelliTrace](https://msdn.microsoft.com/7657ecab-e07e-4b1b-872d-f05d966be37e).  
  
4. **Tamam**'ı tıklatın.  
  
   Bu seçenekler hakkında daha fazla bilgi için bkz. [genel, hata ayıklama, Seçenekler iletişim kutusu](../debugger/general-debugging-options-dialog-box.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Düzenle ve Devam Et](../debugger/edit-and-continue.md)
