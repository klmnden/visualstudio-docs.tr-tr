---
title: 'Nasıl yapılır: ClickOnce dağıtımları için ayrıntılı günlük dosyası belirtme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- logs, ClickOnce deployment
- ClickOnce deployment, logging
ms.assetid: 0807a28d-2e40-4a51-ab10-308d808ded6b
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0efd71b38d3fcd8ae8241e31e721bd48e857d3bd
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754173"
---
# <a name="how-to-specify-verbose-log-files-for-clickonce-deployments"></a>Nasıl yapılır: ClickOnce Dağıtımları İçin Ayrıntılı Günlük Dosyası Belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] tüm dağıtımlar için etkinlik günlük dosyalarını korur. Bu günlükler yükleme, başlatma, güncelleştirme ve kaldırma için ilgili belge ayrıntılarını bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] dağıtım. Ayrıntı düzeyini, [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] bu günlük dosyaları için yazma Kayıt Defteri Düzenleyicisi'ni (**regedit.exe**) ayrıntı düzeyini belirtmek için.  
  
> [!CAUTION]
>  Kayıt Defteri Düzenleyicisi'ni yanlış kullanırsanız, işletim sistemini yeniden yüklemenizi gerektirebilecek önemli sorunlara neden olabilir. Kendi risk altında Kayıt Defteri Düzenleyicisi'ni kullanın.  
  
 Aşağıdaki yordam için ayrıntı düzeyini belirtin açıklar [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] günlük dosyalarını geçerli kullanıcı için. Ayrıntı düzeyini azaltmak için bu kayıt defteri değerini kaldırın.  
  
### <a name="to-specify-verbose-log-files"></a>Ayrıntılı günlük dosyası belirtmek için  
  
1.  Açık **Regedit.exe**.  
  
2.  Düğümüne gidin `HKEY_CURRENT_USER\Software\Classes\Software\Microsoft\Windows\CurrentVersion\Deployment`.  
  
3.  Gerekirse, yeni bir dize değeri adlı oluşturun `LogVerbosityLevel`.  
  
4.  Ayarlama `LogVerbosityLevel` değerini `1`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce Dağıtım Sorunlarını Giderme](../deployment/troubleshooting-clickonce-deployments.md)
