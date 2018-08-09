---
title: Notificação de catálogo de endereços de manusear
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f198be78dd36a6d0c9439da68ab322cd8cfa4172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766660"
---
# <a name="handing-address-book-notification"></a>Notificação de catálogo de endereços de manusear
  
**Aplica-se a**: Outlook 
  
Notificações de catálogo de endereços permitem que um cliente saiba de eventos que ocorrem com qualquer entrada do catálogo de endereços ou como uma entrada específica. Você pode registrar para essas notificações por meio do catálogo de endereços MAPI chamando [IAddrBook::Advise](iaddrbook-advise.md) ou hierarquia de um contêiner catálogo de endereços ou de tabela de conteúdo chamando [IMAPITable::Advise](imapitable-advise.md). 
  
Especifique o identificador de entrada de um contêiner de catálogo de endereços, lista de distribuição ou mensagens de usuário, se você está registrando para notificações em uma entrada específica e NULL se registrando para notificações de catálogo de endereços inteira. O identificador de entrada deve representar um usuário de mensagens ou a lista de distribuição em um contêiner de catálogo de endereços. **IAddrBook::Advise** examina esse identificador de entrada para determinar qual endereço do provedor de catálogo é responsável pelo objeto correspondente e encaminha a chamada ao método de [IABLogon::Advise](iablogon-advise.md) do provedor de catálogo de endereço apropriado. 
  
Os clientes podem se inscrever para os seguintes tipos de eventos de entradas do catálogo de endereços:
  
- Erro crítico
    
- Qualquer um dos eventos de objeto (criado, modificado, excluído, movido ou copiadas)
    
- Tabela modificada
    
Normalmente, o registro ocorre apenas no conteúdo do recipiente de catálogo de endereços e tabelas de hierarquias. É rara que clientes registrar os objetos de usuário e a distribuição da lista de mensagens com nível inferior. Isso acontece porque:
  
- Muitos provedores de catálogo de endereços não dão suporte a notificações em suas mensagens de usuários e listas de distribuição.
    
- Notificações de tabela são suficientes para o controle de alterações e relatórios-las aos usuários.
    

