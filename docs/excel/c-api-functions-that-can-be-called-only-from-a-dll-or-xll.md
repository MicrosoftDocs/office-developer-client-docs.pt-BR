---
title: Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções [excel 2007], api c chamada de dll ou xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765266"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A API C fornece funções de retorno de chamada do Microsoft Excel 15 que só podem ser chamadas usando o **Excel4**, **Excel4v**, **Excel12**ou funções **Excel12v** (ou uma dessas funções indiretamente usando as funções de Framework **Excel **ou **Excel12f**). Isso significa que só pode ser chamados por um DLL ou XLL.
  
## <a name="in-this-section"></a>Nesta seção

[xlAbort](xlabort.md)
  
[xlAsyncReturn](xlasyncreturn.md)
  
[xlCoerce](xlcoerce.md)
  
[xlDefineBinaryName](xldefinebinaryname.md)
  
[xlDisableXLMsgs](xldisablexlmsgs.md)
  
[xlEnableXLMsgs](xlenablexlmsgs.md)
  
[xlEventRegister](xleventregister.md)
  
[xlFree](xlfree.md)
  
[xlGetBinaryName](xlgetbinaryname.md)
  
[xlGetHwnd](xlgethwnd.md)
  
[xlGetInst](xlgetinst.md)
  
[xlGetInstPtr](xlgetinstptr.md)
  
[xlGetName](xlgetname.md)
  
[xlRunningOnCluster](xlrunningoncluster.md)
  
[xlSet](xlset.md)
  
[xlSheetId](xlsheetid.md)
  
[xlSheetNm](xlsheetnm.md)
  
[xlStack](xlstack.md)
  
[xlUDF](xludf.md)
  
## <a name="see-also"></a>Confira também



[C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)

