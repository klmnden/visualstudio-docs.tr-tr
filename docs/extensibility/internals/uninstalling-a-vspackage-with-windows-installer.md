---
title: Windows Installer ile VSPackage kaldırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- packages, uninstalling
- VSPackages, uninstalling
- uninstalling VSPackages
ms.assetid: c4575ac7-82da-4af8-a375-ea756a101fbf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b5f75ee93b856442fd12560d198086489668fd9d
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63429856"
---
# <a name="uninstalling-a-vspackage-with-windows-installer"></a>Windows Installer ile VSPackage Kaldırma
Çoğunlukla, Windows Installer, VSPackage'ı yalnızca göre kaldırabilirsiniz ", VSPackage'ı yüklemek için kişiselleştirmeden geri alma". Özel Eylemler ele [komutları, gerekir olması çalıştırma sonra yükleme](../../extensibility/internals/commands-that-must-be-run-after-installation.md) bir kaldırma işleminden sonra çalıştırılmalıdır. Devenv.exe çağrıları hem yüklenmesi veya kaldırılması için InstallFinalize standart eylem hemen önce gerçekleşmesi için özel ve InstallExecuteSequence tablo girişleri her iki durumda hizmet.

> [!NOTE]
> Çalıştırma `devenv /setup` bir MSI paketi kaldırdıktan sonra.

 Özel Eylemler bir Windows Installer paketini eklerseniz, genel bir kural olarak, bu eylemlerin kaldırma ve geri alma sırasında işlemesi gerekir. Örneğin, VSPackage'ı kendi kendine kaydettirmek için özel eylemler eklerseniz, çok kaydını kaldırmak için özel eylemler eklemeniz gerekir.

> [!NOTE]
> Bir kullanıcı, VSPackage'ı yükleyin ve ardından sürümleri kaldırmak mümkündür [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ile tümleşik olduğundan. Üzerinde çalışan kod bağımlılıkları olan özel eylemler ortadan kaldırarak, VSPackage'nın kaldırılması bu senaryoda çalıştığından emin olun yardımcı [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

## <a name="handling-launch-conditions-at-uninstall-time"></a>İşleme sırasında başlatma koşulları kaldırması
 Hatayı göstermek için LaunchCondition tablonun satırlarını LaunchConditions standart işlemi okur koşullar karşılanmazsa iletileri. Başlatma koşulları emin olmak için sistem gereksinimleri karşılanmadığı, koşul ekleyerek başlatma koşulları kaldırma sırasında genellikle atlayabilirsiniz genellikle kullanıldığından `NOT Installed`, LaunchCondition tablonun LaunchConditions satır.

 Alternatif eklemektir `OR Installed` kaldırma sırasında önemli olmayan Koşulları'nı başlatmak için. Koşul kaldırma sırasında her zaman true olur ve bu nedenle başlatma koşulu hata iletisini görüntülemez sağlar.

> [!NOTE]
> `Installed` Windows Installer, VSPackage'ı sistemde zaten yüklü olduğunu algıladığında ayarlar özelliğidir.

## <a name="see-also"></a>Ayrıca Bkz.
- [Windows Installer](https://msdn.microsoft.com/library/187d8965-c79d-4ecb-8689-10930fa8b3b5)
- [Sistem Gereksinimlerini Algılama](../../extensibility/internals/detecting-system-requirements.md)