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
ms.openlocfilehash: ce0e109aad52bfc4d7f4f55abfe1001d76276f64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587128"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Permite que os visualizadores de formulário trabalhar com contextos de modo de exibição de formulário e notificação de formulário, para executar os verbos de formulário e para serem desligados formulários.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de formulário  <br/> |
|Implementada por:  <br/> |Servidores de formulário  <br/> |
|Chamado pelo:  <br/> |Visualizadores de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIForm  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Estabelece um contexto de modo de exibição para o formulário.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Retorna o contexto de modo de exibição atual para o formulário.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Fecha o formulário.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Solicita que o formulário execute qualquer item das tarefas ele associa um verbo específico.  <br/> |
|[Aviso](imapiform-advise.md) <br/> |Registra um visualizador de formulário para notificações de eventos que afetam o formulário.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Cancela um registro para notificações com um visualizador de formulário que tenha estabelecido chamando **Advise**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem ao objeto form.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

