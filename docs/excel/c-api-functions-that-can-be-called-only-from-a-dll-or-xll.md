---
title: Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api called from dll or xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6d2d3c824c482e3726cdaefa869393002a80f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423115"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A API de C fornece 15 funções de retorno de chamada do Microsoft Excel que só podem ser chamadas usando as funções **Excel4**, **Excel4v**, **Excel12** ou **Excel12v** (ou por uma dessas funções indiretamente usando as funções de estrutura **Excel** ou **Excel12f**). Isso significa que eles só podem ser chamados de uma DLL ou XLL.
  
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



[Retorno de chamada da API de C: funções Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)

