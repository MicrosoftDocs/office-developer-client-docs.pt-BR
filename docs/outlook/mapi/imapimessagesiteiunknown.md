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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433364"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Manipula mensagens e é implementado pelo código do visualizador de formulário (normalmente um aplicativo cliente) que responde a essa manipulação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform.h  <br/> |
|Exposto por:  <br/> |Objetos de site de mensagens  <br/> |
|Implementado por:  <br/> |Visualizadores de formulário  <br/> |
|Chamado por:  <br/> |Objetos de formulário  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIMessageSite  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Retorna a sessão MAPI na qual a mensagem atual foi criada ou aberta.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Retorna o armazenamento de mensagens que contém a mensagem atual, se tal armazenamento existir.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Retorna a pasta na qual a mensagem atual foi criada ou aberta, se tal pasta existir.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Retorna a mensagem atual.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Retorna uma interface do gerenciador de formulário, que um servidor de formulário pode usar para abrir outro servidor de formulário.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Cria uma nova mensagem.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copia a mensagem atual para uma pasta.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Move a mensagem atual para uma pasta.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Exclui a mensagem atual.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Solicita que a mensagem atual seja salva.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Solicita que a mensagem atual seja en fila para entrega.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Retorna informações de um objeto de site de mensagem sobre os recursos do site de mensagens para a mensagem atual.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu no objeto do site de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

