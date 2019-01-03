---
title: 'Nasıl Yapılır: Düzenleyici odağı kaybettiğinde olayları yangın | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - fire events on losing focus
ms.assetid: 64d40695-6917-468a-8037-a253453ac159
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d579b30c5eac25c815739149d3b3baacc22dc439
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53990772"
---
# <a name="how-to-fire-events-when-the-editor-loses-focus"></a>Nasıl Yapılır: Düzenleyici odağı kaybettiğinde olayları tetiklemesine
Bazen bir düzenleyici penceresi çerçevesinde odağı kaybettiğinde öğrenmek gereklidir. Örneğin, düzenleyici artık üzerinde odaklanmıştır sonra bir kod penceresinde kodu ayıklamak gerekebilir. Aşağıdaki yordam, odak kaybetme Düzenleyicisi bildirim almak için izlemeniz gereken adımlar sağlar.  
  
## <a name="to-fire-an-event-in-response-to-an-editor-losing-focus"></a>Bir olay yanıt odak kaybetmeden bir düzenleyici olarak harekete geçirmek için  
  
1.  İzleme seçimi olayları elde ederek bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection> nesnesinden <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection>.  
  
2.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.AdviseSelectionEvents%2A> ve verin, <xref:Microsoft.VisualStudio.Shell.Interop.IVsSelectionEvents> nesne.  
  
3.  Çağrıda <xref:Microsoft.VisualStudio.Shell.Interop.IVsSelectionEvents.OnElementValueChanged%2A>, Aranan `elementid==SEID_WindowFrame`.  
  
4.  Test `varValueNew` parametresi iki şey için:  
  
    1.  Aradığınız pencere çerçevesi.  
  
    2.  Bu pencere çerçevesinin seçimi, programınızı kaybeder noktası.