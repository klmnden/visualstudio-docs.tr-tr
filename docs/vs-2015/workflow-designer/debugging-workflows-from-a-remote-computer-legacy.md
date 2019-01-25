---
title: Uzak bir bilgisayardan (eski) iş akışlarında hata ayıklama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- workflows, debugging remotely
- debugging workflows, remotely
- remote debugging, workflows
- debugging, remote
ms.assetid: 44eaec8f-9959-4ae7-a374-670946f933c1
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f37e2f1d785399283e9da8f4ecb853f0728d9830
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54767513"
---
# <a name="debugging-workflows-from-a-remote-computer-legacy"></a>Uzak Bir Bilgisayardan İş Akışlarında Hata Ayıklama (Eski)
Bu konu, uzak eski hata ayıklama açıklar [!INCLUDE[wf](../includes/wf-md.md)] eski ile oluşturulan uygulamalar [!INCLUDE[wfd1](../includes/wfd1-md.md)]. Eski kullanın [!INCLUDE[wfd2](../includes/wfd2-md.md)] gerektiğinde uygulamanızı ya da hedef [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] veya [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
 Yüklediğinizde [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)], bileşeni yükleme seçeneklerden biri yüklenecek [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] için hata ayıklayıcı [!INCLUDE[wf](../includes/wf-md.md)]. Bu, uzaktan hata ayıklama bileşenleri yükler. Bu uzaktan hata ayıklama bileşenlerini, uzak iş akışı hata ayıklama için hedeflediğiniz bilgisayara yüklenmelidir.  
  
 Ayrıca, uzak bir bilgisayarda hata ayıklaması yaptığınız eski iş akışı tanımı içeren derleme genel derleme önbelleğinde (GAC) hata ayıklaması yapıyorsanız yerel bilgisayarın yüklenmelidir. Örneğin, bir uzak bir bilgisayarda eski bir iş akışını çalıştıran ve yerel bilgisayardan B ayıkladığınız, iş akışı tanımı GAC'ye b bilgisayarının bulunması gerekir Bu seri durumdan ve B bilgisayarında bilgisayarına uzaktan çalışan iş akışının iş akışı biçimlendirmesi görüntülemek tasarımcı sağlar Genel Derleme Önbelleği hakkında daha fazla bilgi için bkz. MSDN Kitaplığı.  
  
 [!INCLUDE[wf2](../includes/wf2-md.md)] Uzaktan hata ayıklama, İşlevler için uzaktan hata ayıklama ile aynı [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] bileşenleri. Daha fazla bilgi için [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] MSDN Kitaplığı'nda uzaktan hata ayıklama.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski İş Akışlarında Hata Ayıklama](../workflow-designer/debugging-legacy-workflows.md)