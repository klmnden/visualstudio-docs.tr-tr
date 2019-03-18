---
title: Idebugapplication arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplication interface
ms.assetid: 5dfa941b-4cd9-46fa-a230-3f41df9ea205
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8229f234f8a8ce607f36c48e070cb3d40a211d45
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58152476"
---
# <a name="idebugapplication-interface"></a>IDebugApplication Arabirimi
Uzaktan olmayan hata ayıklama yöntemleri kullanmak için dil altyapıları ve konakları kullanımına sunar.  
  
 Devralınan yöntemleri yanı sıra `IRemoteDebugApplication`, `IDebugApplication` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugApplication::SetName](../../winscript/reference/idebugapplication-setname.md)|Uygulama adını ayarlar.|  
|[IDebugApplication::StepOutComplete](../../winscript/reference/idebugapplication-stepoutcomplete.md)|İşlem Hata Ayıklama Yöneticisi tek adımlı modda bir dil altyapısı hakkında arayanına döndürülecek olduğunu bildirir.|  
|[IDebugApplication::DebugOutput](../../winscript/reference/idebugapplication-debugoutput.md)|IDE hata ayıklayıcı tarafından görüntülenecek verilen dize neden olur.|  
|[IDebugApplication::StartDebugSession](../../winscript/reference/idebugapplication-startdebugsession.md)|IDE varsayılan hata ayıklayıcıyı başlatır ve değil bir zaten bağlıysa, bu uygulama için bir hata ayıklama oturumu ekler.|  
|[IDebugApplication::HandleBreakPoint](../../winscript/reference/idebugapplication-handlebreakpoint.md)|Geçerli iş parçacığını engellemek neden olur ve IDE hata ayıklayıcı kesme noktası bir bildirim gönderir.|  
|[IDebugApplication::Close](../../winscript/reference/idebugapplication-close.md)|Tüm başvuruları bırakın ve etkin olmayan bir duruma girmek bu uygulamanın neden olur.|  
|[IDebugApplication::GetBreakFlags](../../winscript/reference/idebugapplication-getbreakflags.md)|Uygulama için geçerli kesme bayrakları döndürür.|  
|[IDebugApplication::GetCurrentThread](../../winscript/reference/idebugapplication-getcurrentthread.md)|Şu anda çalışan iş parçacığı ile ilişkili iş parçacığı döndürür.|  
|[IDebugApplication::CreateAsyncDebugOperation](../../winscript/reference/idebugapplication-createasyncdebugoperation.md)|Belirli bir zaman uyumlu hata ayıklama işlemi zaman uyumsuz erişim sağlar.|  
|[IDebugApplication::AddStackFrameSniffer](../../winscript/reference/idebugapplication-addstackframesniffer.md)|Bu uygulama için bir yığın çerçevesi Numaralandırıcı sağlayıcısı ekler.|  
|[IDebugApplication::RemoveStackFrameSniffer](../../winscript/reference/idebugapplication-removestackframesniffer.md)|Bir yığın çerçevesi Numaralandırıcı sağlayıcısı bu uygulamadan kaldırır.|  
|[IDebugApplication::QueryCurrentThreadIsDebuggerThread](../../winscript/reference/idebugapplication-querycurrentthreadisdebuggerthread.md)|Geçerli çalışan iş parçacığı hata ayıklayıcı iş parçacığı olup olmadığını belirler.|  
|[IDebugApplication::SynchronousCallInDebuggerThread](../../winscript/reference/idebugapplication-synchronouscallindebuggerthread.md)|Çağıran kod hata ayıklayıcı iş parçacığında çalıştırmak bir mekanizma sağlar.|  
|[IDebugApplication::CreateApplicationNode](../../winscript/reference/idebugapplication-createapplicationnode.md)|Belirli bir belge sağlayıcı ile ilişkili yeni bir uygulama düğümü oluşturur.|  
|[IDebugApplication::FireDebuggerEvent](../../winscript/reference/idebugapplication-firedebuggerevent.md)|Hata Ayıklayıcı'nın için genel bir olay harekete `IApplicationDebugger` arabirimi.|  
|[IDebugApplication::HandleRuntimeError](../../winscript/reference/idebugapplication-handleruntimeerror.md)|Geçerli iş parçacığını engellemek neden olur ve hata ayıklayıcıya IDE hatanın bir bildirim gönderir.|  
|[IDebugApplication::FCanJitDebug](../../winscript/reference/idebugapplication-fcanjitdebug.md)|Just-ın-time (JIT) hata ayıklayıcı kayıtlı olup olmadığını belirler.|  
|[IDebugApplication::FIsAutoJitDebugEnabled](../../winscript/reference/idebugapplication-fisautojitdebugenabled.md)|JIT hata ayıklayıcı otomatik hata ayıklama dumb Konaklara kayıtlıysa belirler.|  
|[IDebugApplication::AddGlobalExpressionContextProvider](../../winscript/reference/idebugapplication-addglobalexpressioncontextprovider.md)|Bu uygulama için bir genel ifade içeriği sağlayıcısı ekler.|  
|[IDebugApplication::RemoveGlobalExpressionContextProvider](../../winscript/reference/idebugapplication-removeglobalexpressioncontextprovider.md)|Genel ifade bağlam sağlayıcı bu uygulamadan kaldırır.|