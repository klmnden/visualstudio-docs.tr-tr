---
title: Proje türlerini dağıtma | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- projects [Visual Studio SDK], managed-code
- projects [Visual Studio SDK], aggregator
ms.assetid: 7f132f67-8589-464c-90dc-0d57ae02aa8f
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b54250a32c8c3a24232d2b6a654aeb87fa9a727b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49188260"
---
# <a name="deploying-project-types"></a>Proje Türlerini Dağıtma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

[!INCLUDE[vsipsdk](../../includes/vsipsdk-md.md)] Yeni bir proje türü toplayıcısı (ProjectAggregator2.dll) ve ayrıca yeniden dağıtımı (ProjectAggregator2.msi) için bir Windows Installer paketi yükler. Yönetilen kod proje türleri için yeni Toplayıcısı'nı kullanmanız gerekir. ProjectAggregator2 çalışır geçici çözüm sınırlamaları [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] yönetilen kod proje türleri düzgün çalışmasını engelleyen toplayıcısı proje. Aşağıdaki adımlar, yeni Toplayıcı'yı kullanmak için VSPackage değiştirmek açıklanmaktadır.  
  
1.  NativeHierarchyWrapper proje çözümünüzden kaldırın.  
  
2.  Herhangi bir NativeHierarchyWrapper ikili kurulumunuzu kaldırın.  
  
3.  ProjectAggregator2.msi kurulumunuzu ekleyin.

