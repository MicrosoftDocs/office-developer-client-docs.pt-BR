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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299500"
---
# <a name="handing-address-book-notification"></a>Manipula notificações do catálogo de endereços
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As notificações do catálogo de endereços permitem que um cliente Aprenda eventos que ocorrem a qualquer entrada do catálogo de endereços ou a uma entrada específica. Você pode registrar essas notificações por meio do catálogo de endereços MAPI chamando [IAddrBook:: Advise](iaddrbook-advise.md) ou por meio de uma hierarquia de conteúdo do contêiner de catálogo de endereços ou tabela de conteúdo chamando IMAPITable [:: Advise](imapitable-advise.md). 
  
Especifique o identificador de entrada de um contêiner de catálogo de endereços, lista de distribuição ou usuário de mensagens se você estiver se registrando para notificações em uma determinada entrada e nulo se estiver se registrando para notificações em todo o catálogo de endereços. O identificador de entrada deve representar um usuário de mensagens ou uma lista de distribuição em um contêiner de catálogo de endereços. **IAddrBook:: Advise** examina esse identificador de entrada para determinar qual provedor de catálogo de endereços é responsável pelo objeto correspondente e encaminha a chamada para o método [IABLogon:: Advise](iablogon-advise.md) do provedor de catálogo de endereços apropriado. 
  
Os clientes podem se registrar nos seguintes tipos de eventos nas entradas do catálogo de endereços:
  
- Erro crítico
    
- Qualquer um dos eventos de objeto (criado, modificado, excluído, movido ou copiado)
    
- Tabela modificada
    
Normalmente, o registro ocorre somente no conteúdo do contêiner do catálogo de endereços e tabelas de hierarquia. É raro que os clientes sejam registrados com o usuário de sistema de mensagens de nível inferior e os objetos de lista de distribuição. Isso ocorre porque:
  
- Muitos provedores de catálogo de endereços não dão suporte a notificações em seus usuários de mensagens e listas de distribuição.
    
- As notificações de tabela são suficientes para controlar alterações e relatá-las aos usuários.
    

