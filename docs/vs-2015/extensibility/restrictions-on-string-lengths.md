---
title: Dize uzunluğu kısıtlamaları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, restrictions on string lengths
ms.assetid: 877173d2-ca27-43b3-b1f4-8379f7c5e268
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: dc6ff1e77a9a973e184384d98ef8b880aaa2f005
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432531"
---
# <a name="restrictions-on-string-lengths"></a>Dize Uzunluğu Kısıtlamaları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kaynak Denetimi Eklentisi API çeşitli işlevler için kullanılan dizelerin uzunluklarının sınırlar.  
  
## <a name="string-length-values"></a>Dize uzunluğu değerleri  
  
|Sabit|Değer|  
|--------------|-----------|  
|`SCC_NAME_LEN`|31|  
|`SCC_AUXLABEL_LEN`|31|  
|`SCC_USER_LEN`|31|  
|`SCC_PRJPATH_LEN`|300|  
  
> [!NOTE]
> Uzunluğu sonlandırma içermez `null`. Bir "_LEN" yerine "_boyut" soneki ile diğer sabitleri sonlandırmak için boşluk `null`.  
  
|Sabit|Değer|  
|--------------|-----------|  
|SCC_NAME_SIZE|32|  
|SCC_AUXLABEL_SIZE|32|  
|SCC_USER_SIZE|32|  
|SCC_PRJPATH_SIZE|301|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentileri](../extensibility/source-control-plug-ins.md)
