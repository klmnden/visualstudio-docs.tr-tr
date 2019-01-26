---
title: Proje türlerini dağıtma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], managed-code
- projects [Visual Studio SDK], aggregator
ms.assetid: 7f132f67-8589-464c-90dc-0d57ae02aa8f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b42e4f879352a6edaf9171296b282accd9b1ae3f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55009914"
---
# <a name="deploy-project-types"></a>Proje türlerini dağıtma
[!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] Yeni bir proje türü toplayıcısı yükler (*ProjectAggregator2.dll*) ve yeniden dağıtım için de bir Windows Installer paketi (*ProjectAggregator2.msi*). Yönetilen kod proje türleri için yeni Toplayıcısı'nı kullanmanız gerekir. ProjectAggregator2 çalışır kısıtlamaları geçici [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] yönetilen kod proje türleri düzgün çalışmasını engeller toplayıcısı proje. Aşağıdaki adımlar, yeni Toplayıcı'yı kullanmak için VSPackage değiştirmek açıklanmaktadır.  
  
1.  NativeHierarchyWrapper proje çözümünüzden kaldırın.  
  
2.  Herhangi bir NativeHierarchyWrapper ikili kurulumunuzu kaldırın.  
  
3.  Ekleme *ProjectAggregator2.msi* kurulumunuzu için.