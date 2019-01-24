---
title: IDebugDocumentChecksum2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugDocumentChecksum2 interface
ms.assetid: 6d22fa94-21aa-46cb-b5b5-32a6399ebb20
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ba1510745b4781d56655fe83fffbb18f4ca65254
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54777985"
---
# <a name="idebugdocumentchecksum2"></a>IDebugDocumentChecksum2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Hata ayıklama belge için bir sağlama toplamı temsil eder ve bileşenleri arasında sağlama toplamı geçirme sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugDocumentChecksum2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirimi kullanıma sunan herhangi bir bileşeni tarafından uygulanabilir [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md) arabirimi. Ancak, katıştırılmış bir sembol dosyası (*.pdb) sağlama toplamı IDE geçirilen ve bir kaynağı bulma işleminde kullanılan hata ayıklama motoru tarafından temelde uygulandığı.  
  
## <a name="methods"></a>Yöntemler  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugDocumentChecksum2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetChecksumAndAlgorithmId](../../../extensibility/debugger/reference/idebugdocumentchecksum2-getchecksumandalgorithmid.md)|Kullanılacak bayt sayısı belirtilen belge sağlama toplamı ve algoritma tanımlayıcısını alır.|  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll
