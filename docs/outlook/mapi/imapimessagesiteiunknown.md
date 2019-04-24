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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321347"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Manipula mensagens e é implementada pelo código de visualização de formulário (normalmente, um aplicativo cliente) que responde a tal manipulação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
|Exposto por:  <br/> |Objetos de site de mensagens  <br/> |
|Implementado por:  <br/> |Visualizadores de formulários  <br/> |
|Chamado por:  <br/> |Objetos de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIMessageSite  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Retorna a sessão MAPI na qual a mensagem atual foi criada ou aberta.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Retorna o repositório de mensagens que contém a mensagem atual, se esse repositório existir.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Retorna a pasta na qual a mensagem atual foi criada ou aberta, se essa pasta existir.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Retorna a mensagem atual.  <br/> |
|[GetFormmanager](imapimessagesite-getformmanager.md) <br/> |Retorna uma interface de Gerenciador de formulários, que um servidor de formulário pode usar para abrir outro servidor de formulários.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Cria uma nova mensagem.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copia a mensagem atual para uma pasta.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Move a mensagem atual para uma pasta.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Exclui a mensagem atual.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Solicita que a mensagem atual seja salva.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Solicita que a mensagem atual seja enfileirada para entrega.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Retorna informações de um objeto de site de mensagem sobre os recursos do site da mensagem para a mensagem atual.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto site da mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

