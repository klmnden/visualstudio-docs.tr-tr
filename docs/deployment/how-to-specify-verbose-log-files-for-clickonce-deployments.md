---
title: 'Nasıl yapılır: ClickOnce dağıtımları için ayrıntılı günlük dosyası belirtme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- logs, ClickOnce deployment
- ClickOnce deployment, logging
ms.assetid: 0807a28d-2e40-4a51-ab10-308d808ded6b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d57c9aa618ec3df91b130cb2f870d88b01c323c2
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63406700"
---
# <a name="how-to-specify-verbose-log-files-for-clickonce-deployments"></a>Nasıl yapılır: ClickOnce dağıtımları için ayrıntılı günlük dosyası belirtme
[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] tüm dağıtımlar için etkinlik günlük dosyalarını korur. Bu günlükler yükleme, başlatma, güncelleştirme ve kaldırma için ilgili belge ayrıntılarını bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] dağıtım. Ayrıntı düzeyini, [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] bu günlük dosyaları için yazma Kayıt Defteri Düzenleyicisi'ni (*regedit.exe*) ayrıntı düzeyini belirtmek için.

> [!CAUTION]
> Kayıt Defteri Düzenleyicisi'ni yanlış kullanırsanız, işletim sistemini yeniden yüklemenizi gerektirebilecek önemli sorunlara neden olabilir. Kendi risk altında Kayıt Defteri Düzenleyicisi'ni kullanın.

 Aşağıdaki yordam için ayrıntı düzeyini belirtin açıklar [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] günlük dosyalarını geçerli kullanıcı için. Ayrıntı düzeyini azaltmak için bu kayıt defteri değerini kaldırın.

### <a name="to-specify-verbose-log-files"></a>Ayrıntılı günlük dosyası belirtmek için

1. Açık *Regedit.exe*.

2. Düğümüne gidin **HKEY_CURRENT_USER\Software\Classes\Software\Microsoft\Windows\CurrentVersion\dağıtım**.

3. Gerekirse, yeni bir dize değeri adlı oluşturun `LogVerbosityLevel`.

4. Ayarlama `LogVerbosityLevel` değerini `1`.

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce dağıtım sorunlarını giderme](../deployment/troubleshooting-clickonce-deployments.md)