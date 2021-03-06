---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436381"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que os visualizadores de formulários trabalhem com contextos de modo de formulário e notificação de formulário, executem verbos de formulário e desliguem formulários.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform.h  <br/> |
|Exposto por:  <br/> |Objetos de formulário  <br/> |
|Implementado por:  <br/> |Servidores de formulário  <br/> |
|Chamado por:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIForm  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Estabelece um contexto de exibição para o formulário.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Retorna o contexto de exibição atual do formulário.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Fecha o formulário.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Solicita que o formulário execute as tarefas associadas a um verbo específico.  <br/> |
|[Advise](imapiform-advise.md) <br/> |Registra um visualizador de formulário para notificações sobre eventos que afetam o formulário.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Cancela um registro para notificações com um visualizador de formulário estabelecido anteriormente chamando **Advise**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu no objeto de formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

