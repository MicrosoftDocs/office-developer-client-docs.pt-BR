---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 75ef8d6f2134e0269745f92dab1f790228692853
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767107"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite: IUnknown

  
  
**Aplica-se a**: Outlook 
  
Manipula mensagens e é implementada com o código do Visualizador de formulário (geralmente, um aplicativo cliente) que responde a tal manipulação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de site  <br/> |
|Implementada por:  <br/> |Visualizadores de formulário  <br/> |
|Chamado pelo:  <br/> |Objetos de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIMessageSite  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Retorna a sessão MAPI em que a mensagem atual foi criada ou aberta.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Retorna o repositório de mensagem que contém a mensagem atual, se existir um repositório tal.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Retorna a pasta na qual a mensagem atual foi criada ou aberta, se existir uma pasta tal.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Retorna a mensagem atual.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Retorna uma interface de Gerenciador de formulário, que um servidor de formulário pode usar para abrir o outro servidor de formulário.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Cria uma nova mensagem.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copia a mensagem atual para uma pasta.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Move a mensagem atual para uma pasta.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Exclui a mensagem atual.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Solicita que a mensagem atual seja salvo.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Solicita que a mensagem atual ser colocados na fila de entrega.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Retorna informações de um objeto de site de mensagem sobre a mensagem de recursos do site da mensagem atual.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o que ocorrem ao objeto de site de mensagem de erro anterior.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

