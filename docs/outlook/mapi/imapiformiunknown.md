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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: fce8bc45d5cc87c238288653ab989b62076ad451
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767045"
---
# <a name="imapiform--iunknown"></a>IMAPIForm: IUnknown

  
  
**Aplica-se a**: Outlook 
  
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

