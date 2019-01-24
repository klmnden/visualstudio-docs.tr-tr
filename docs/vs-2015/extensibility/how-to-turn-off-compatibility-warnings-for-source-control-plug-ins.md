---
title: 'Nasıl yapılır: Kaynak denetimi eklentileri için uyumluluk uyarılarını kapatma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, turning off compatibility warnings
- compatibility warnings, turning off
ms.assetid: ba318e12-921b-4b7a-a8c2-12c712be1dbf
caps.latest.revision: 22
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 9efe961774ef1939cfc95c2efe9146a59e46bc17
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54783701"
---
# <a name="how-to-turn-off-compatibility-warnings-for-source-control-plug-ins"></a>Nasıl yapılır: Kaynak Denetimi Eklentileri için Uyumluluk Uyarılarını Kapatma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir kullanıcı birden fazla uyumluluk uyarılarını görebilirsiniz, kaynak denetiminde yoksayılacaktır [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Sunulan uyarılar, kaynak denetimi eklentisi yeteneklerine bağlıdır ve ayrıntılı buraya devre dışı bırakılabilir.  
  
### <a name="to-disable-the-warning-to-ensure-optimal-source-control-integration-with-visual-studio"></a>Uyarıyı devre dışı bırakmak için: "... En iyi kaynak denetimi tümleştirmesi Visual Studio ile sağlamak için"  
  
-   (Gerekirse değeri ekleyerek) aşağıdaki kayıt defteri girdisini ayarlayın:  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\DontDisplayCheckDotNETCompatible = DWORD: 00000001  
  
     Tüm bu uyarı görüntülenir olmayan[!INCLUDE[vsvss](../includes/vsvss-md.md)] eklentiler.  
  
### <a name="to-disable-the-warning-the-installed-source-control-provider-does-not-support-all-the-capabilities"></a>Uyarıyı devre dışı bırakmak için: "Kurulan kaynak denetim sağlayıcısı tüm özellikleri... desteklemiyor"  
  
-   (Değer gerekirse ekleme), aşağıdaki iki kayıt defteri değerlerini ayarlayın:  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\WarnedOldMSSCCIProvider = DWORD: 00000000  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\UseOldSCC = dword:00000001  
  
     (Diğer bir deyişle, yalnızca bir dosya ve proje aynı anda denetleyebilir,) kaynak denetimi eklentisi açıkça yeniden giriş için birden çok proje desteklemiyorsa bu uyarı görüntülenir.  
  
     Yeniden giriş desteklemek en iyi (`SCC_CAP_REENTRANT` yeteneği); bunu yapmak kadar bu uyarıyı kaldırmak. Ancak, bu destek mümkün değilse, bu kayıt defteri girişleri ayarlanabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özellik Bayrakları](../extensibility/capability-flags.md)
