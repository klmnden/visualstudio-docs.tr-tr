---
title: Projeleri genişletme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- solutions [Visual Studio]
- projects [Visual Studio]
ms.assetid: 096d273d-4fe9-4f24-9b00-470bfbdf4bdf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d31da41e3be73f4e2e036841bfc1d96f4476e856
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62912811"
---
# <a name="extend-projects"></a>Projeleri genişletme
Projeler ve çözümler, Visual Studio kodu ve kaynak dosyaları derleme ve dağıtım birimler halinde düzenler yöntemleri sunulmaktadır. Projeler hakkında daha fazla bilgi bulabilirsiniz [projeleri (Visual Studio SDK)](../extensibility/extending-projects.md).

 Visual Studio SDK'sı ve yönetilen paket çerçevesini adresinden indirebilirsiniz projeleri için kendi proje türleri oluşturma [projeleri için yönetilen paket çerçevesini](https://github.com/tunnelvisionlabs/MPFProj10). Anlamak için özel projeler uygulanan edinmek bkz [yeni proje oluşturma: Bir altyapı öğeleri, bölüm](../extensibility/internals/new-project-generation-under-the-hood-part-one.md) ve [yeni proje oluşturma: Altyapı öğeleri, bölüm iki](../extensibility/internals/new-project-generation-under-the-hood-part-two.md).

 Bu bölümdeki konular, özel Proje nasıl oluşturulacağını ve Visual Studio çözümünün farklı türlerini yönetme açıklar.

## <a name="in-this-section"></a>Bu bölümde
- [1. Bölüm temel proje sistemi oluşturma](../extensibility/creating-a-basic-project-system-part-1.md) özel Proje sistemi oluşturmayı açıklar.

- [2. Bölüm temel proje sistemi oluşturma](../extensibility/creating-a-basic-project-system-part-2.md) özel Proje sistemi oluşturmayı açıklar.

- [Proje dosyalarında verileri kaydetme](../extensibility/saving-data-in-project-files.md) açıklanmaktadır projeye nasıl ekleyin (<em>.</em> Proj *) dosyaları.

- [Çalışma zamanında proje alt türlerini doğrulama](../extensibility/verifying-subtypes-of-a-project-at-run-time.md) çalışma zamanında proje alt doğrulamak kullanılan nasıl açıklanmaktadır.

- [Özellik sayfaları eklemenizi ve kaldırmanızı](../extensibility/adding-and-removing-property-pages.md) özel projeniz için özellik sayfalarını özelleştirme açıklanmaktadır.

- [Bir proje öğesine öznitelik ekleme](../extensibility/adding-an-attribute-to-a-project-item.md) özel proje öğesine öznitelik ekleme işlemi açıklanmaktadır.

- [Proje öğesinin özelliğini kalıcı](../extensibility/persisting-the-property-of-a-project-item.md) bir özel Proje öğesinin özelliğini kalıcı açıklanmaktadır.

- [Evrensel Windows projeleri yönetme](../extensibility/managing-universal-windows-projects.md) Evrensel projelerinin nasıl yönetildiği açıklanır.