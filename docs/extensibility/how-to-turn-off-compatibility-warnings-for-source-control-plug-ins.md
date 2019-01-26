---
title: Kaynak denetimi eklentileri için uyumluluk uyarılarını kapatma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, turning off compatibility warnings
- compatibility warnings, turning off
ms.assetid: ba318e12-921b-4b7a-a8c2-12c712be1dbf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2d90ab2553eb69a5ea429dec3848c2aecd5fa86a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54978808"
---
# <a name="how-to-turn-off-compatibility-warnings-for-source-control-plug-ins"></a>Nasıl yapılır: Kaynak denetimi eklentileri için uyumluluk uyarılarını kapatma
Bir kullanıcı birden fazla uyumluluk uyarılarını görebilirsiniz, kaynak denetiminde yoksayılacaktır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Sunulan uyarılar, kaynak denetimi eklentisi yeteneklerine bağlıdır ve ayrıntılı buraya devre dışı bırakılabilir.  
  
### <a name="to-disable-the-warning-to-ensure-optimal-source-control-integration-with-visual-studio"></a>Uyarıyı devre dışı bırakmak için: "Visual Studio ile en iyi kaynak denetimi tümleştirmesi sağlamak için"  
  
- (Gerekirse değeri ekleyerek) aşağıdaki kayıt defteri girdisini ayarlayın:  
  
   **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\DontDisplayCheckDotNETCompatible = DWORD: 00000001**  
  
   Tüm bu uyarı görüntülenir olmayan[!INCLUDE[vsvss](../extensibility/includes/vsvss_md.md)] eklentiler.  
  
### <a name="to-disable-the-warning-the-installed-source-control-provider-does-not-support-all-the-capabilities"></a>Uyarıyı devre dışı bırakmak için: "Kurulan kaynak denetim sağlayıcısı tüm yetenekleri desteklemiyor"  
  
-   (Değer gerekirse ekleme), aşağıdaki iki kayıt defteri değerlerini ayarlayın:  
  
     **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\WarnedOldMSSCCIProvider = DWORD: 00000000**  
  
    **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\UseOldSCC = DWORD: 00000001**  
  
     (Diğer bir deyişle, yalnızca bir dosya ve proje aynı anda denetleyebilir,) kaynak denetimi eklentisi açıkça yeniden giriş için birden çok proje desteklemiyorsa bu uyarı görüntülenir.  
  
     Yeniden giriş desteklemek en iyi (`SCC_CAP_REENTRANT` yeteneği); bunu yapmak kadar bu uyarıyı kaldırmak. Ancak, bu destek mümkün değilse, bu kayıt defteri girişleri ayarlanabilir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Özellik bayrakları](../extensibility/capability-flags.md)