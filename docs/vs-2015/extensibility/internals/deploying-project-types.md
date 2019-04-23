---
title: Proje türlerini dağıtma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], managed-code
- projects [Visual Studio SDK], aggregator
ms.assetid: 7f132f67-8589-464c-90dc-0d57ae02aa8f
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0fda84d5f7467a65b254d3b12b0466b6ab415d61
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60076478"
---
# <a name="deploying-project-types"></a>Proje Türlerini Dağıtma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

[!INCLUDE[vsipsdk](../../includes/vsipsdk-md.md)] Yeni bir proje türü toplayıcısı (ProjectAggregator2.dll) ve ayrıca yeniden dağıtımı (ProjectAggregator2.msi) için bir Windows Installer paketi yükler. Yönetilen kod proje türleri için yeni Toplayıcısı'nı kullanmanız gerekir. ProjectAggregator2 çalışır geçici çözüm sınırlamaları [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] yönetilen kod proje türleri düzgün çalışmasını engelleyen toplayıcısı proje. Aşağıdaki adımlar, yeni Toplayıcı'yı kullanmak için VSPackage değiştirmek açıklanmaktadır.  
  
1. NativeHierarchyWrapper proje çözümünüzden kaldırın.  
  
2. Herhangi bir NativeHierarchyWrapper ikili kurulumunuzu kaldırın.  
  
3. ProjectAggregator2.msi kurulumunuzu ekleyin.
