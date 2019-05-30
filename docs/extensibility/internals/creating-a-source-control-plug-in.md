---
title: Kaynak Denetimi Eklentisi oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- plug-ins, source control
- source control plug-ins
- source control [Visual Studio SDK], plug-ins
ms.assetid: c7e69fa4-150e-469a-a6fc-fa1260bdbb07
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b8489e991a54df5b905289a64fccb0df65c3cec8
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66341921"
---
# <a name="create-a-source-control-plug-in"></a>Kaynak Denetimi Eklentisi oluşturma
Visual Studio SDK'sı, kaynak denetim yeteneği eklemenize olanak sağlayan kaynaklar sağlayan [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE). Bu belgede özetlenen kaynak denetimi eklentisi API ile uyumlu herhangi bir eklentinin DLL kullanmanıza imkan tanır.

## <a name="in-this-section"></a>Bu bölümde
- [Kullanmaya başlama](../../extensibility/internals/getting-started-with-source-control-plug-ins.md)

 Kaynak Denetimi Eklentisi yükleme açıklar ve şu anda kullanılabilir olan kaynak denetimi eklentisi API sürümlerine vurgular.

- [Mimari](../../extensibility/internals/source-control-plug-in-architecture.md)

 Kaynak denetimi eklentisi ile tümleştirilmesi açıklamak için bir mimari diyagramını kullanır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE.

- [Test Kılavuzu](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)

 Kaynak Denetimi Eklentisi işleyişini ve yükleme testi konusunda rehberlik sağlar.

## <a name="related-sections"></a>İlgili bölümler
- [Kaynak denetimi VSPackage'ı oluşturma](../../extensibility/internals/creating-a-source-control-vspackage.md)

 Kaynak denetimi, yalnızca kaynak denetimi işlevlerini sağlar ancak değiştirir VSPackage'ı oluşturma anlatılmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kaynak UI denetimi.

- [Kaynak denetimi eklentileri](../../extensibility/source-control-plug-ins.md)

 Kaynak Denetimi Eklentisi API içindeki tüm öğelerin tam listesini sağlar.

- [Kaynak denetimi](../../extensibility/internals/source-control.md)

 Tümleşik bir özelliği olarak kaynak denetimi uygulama seçenekleri ele alınmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].
