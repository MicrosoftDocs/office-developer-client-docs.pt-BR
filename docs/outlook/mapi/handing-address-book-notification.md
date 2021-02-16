---
title: Manipula notificações do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413532"
---
# <a name="handing-address-book-notification"></a>Manipula notificações do catálogo de endereços
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As notificações do livro de endereços permitem que um cliente saiba dos eventos que ocorrem em qualquer entrada do livro de endereços ou em uma entrada específica. Você pode se registrar para essas notificações através do livro de endereços MAPI chamando [IAddrBook::Advise](iaddrbook-advise.md) ou por meio da hierarquia ou tabela de conteúdo de um contêiner de agendamento de endereço chamando [IMAPITable::Advise](imapitable-advise.md). 
  
Especifique o identificador de entrada de um contêiner de agendamento de endereço, lista de distribuição ou usuário de mensagens se você estiver se registrando para notificações em uma entrada específica e NULL se estiver se registrando para notificações em todo o livro de endereços. O identificador de entrada deve representar um usuário de mensagens ou uma lista de distribuição em um contêiner de agendamento de endereços. **IAddrBook::Advise** examina esse identificador de entrada para determinar qual provedor de agendamento é responsável pelo objeto correspondente e encaminha a chamada para o método [IABLogon::Advise](iablogon-advise.md) do provedor de agendamento apropriado. 
  
Os clientes podem se registrar para os seguintes tipos de eventos nas entradas do livro de endereços:
  
- Erro crítico
    
- Qualquer um dos eventos de objeto (criados, modificados, excluídos, movidos ou copiados)
    
- Tabela modificada
    
Normalmente, o registro ocorre apenas nos conteúdos do contêiner do address book e nas tabelas de hierarquia. É raro que os clientes se registrem com os objetos de lista de distribuição e usuário de mensagens de nível inferior. Isso porque:
  
- Muitos provedores de agendamento de endereço não suportam notificações em suas listas de distribuição e usuários de mensagens.
    
- As notificações de tabela são suficientes para rastrear alterações e re reportá-las aos usuários.
    

