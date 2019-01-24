---
title: 'Nasıl yapılır: Düzenleyici odağı kaybettiğinde olayları yangın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - fire events on losing focus
ms.assetid: 64d40695-6917-468a-8037-a253453ac159
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c6bcd77d16f3c765a522f178604842714db84e24
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764467"
---
# <a name="how-to-fire-events-when-the-editor-loses-focus"></a>Nasıl yapılır: Düzenleyici odağı kaybettiğinde olayları tetiklemesine
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bazen bir düzenleyici penceresi çerçevesinde odağı kaybettiğinde öğrenmek gereklidir. Örneğin, düzenleyici artık üzerinde odaklanmıştır sonra bir kod penceresinde kodu ayıklamak gerekebilir. Aşağıdaki yordam, odak kaybetme Düzenleyicisi bildirim almak için izlemeniz gereken adımlar sağlar.  
  
### <a name="to-fire-an-event-in-response-to-an-editor-losing-focus"></a>Bir olay yanıt odak kaybetmeden bir düzenleyici olarak harekete geçirmek için  
  
1.  İzleme seçimi olayları elde ederek bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection> nesnesinden <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection>.  
  
2.  Çağrı <xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.AdviseSelectionEvents%2A> ve verin, <xref:Microsoft.VisualStudio.Shell.Interop.IVsSelectionEvents> nesne.  
  
3.  Çağrıda <xref:Microsoft.VisualStudio.Shell.Interop.IVsSelectionEvents.OnElementValueChanged%2A>, Aranan `elementid==SEID_WindowFrame`.  
  
4.  Test `varValueNew` parametresi iki şey için:  
  
    1.  Aradığınız pencere çerçevesi.  
  
    2.  Bu pencere çerçevesinin seçimi, programınızı kaybeder noktası.
