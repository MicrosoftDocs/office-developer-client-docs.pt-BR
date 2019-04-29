---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406028"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gerencia um formulário no Visualizador de formulários de um aplicativo cliente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
|Exposto por:  <br/> |Exibir objetos de contexto  <br/> |
|Implementado por:  <br/> |Visualizadores de formulários  <br/> |
|Chamado por:  <br/> |Objetos de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIViewContext  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Gerencia o registro de um formulário para receber notificações sobre alterações no visualizador.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Ativa a mensagem seguinte ou anterior no Visualizador de formulários.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Recupera as informações de impressão atuais.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Recupera um fluxo a ser usado para salvar a mensagem atual.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Recupera o status atual do visualizador.  <br/> |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre no objeto de contexto View.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

