---
title: Tratamento de sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767948"
---
# <a name="mapi-session-handling"></a>Tratamento de sessão MAPI

  
  
**Aplica-se a**: Outlook 
  
Antes de você poderá se comunicar com provedores de serviço e um sistema de mensagens subjacente, você precisa estabelecer uma sessão. Uma sessão MAPI é um vínculo de um cliente para outros componentes MAPI. Como resultado de iniciando com êxito uma sessão, MAPI retorna aos clientes um ponteiro para um objeto de sessão — um objeto que implementa a interface **IMAPISession** . Para obter mais informações, consulte [IMAPISession: IUnknown](imapisessioniunknown.md). Você pode usar os métodos da interface **IMAPISession** para acessar os objetos de provedores de armazenamento de mensagens e catálogo de endereço, acessar várias tabelas, formulários de exibição, definir propriedades de provedor de transporte e executar a administração de serviço de perfil e mensagem. 
  
## <a name="in-this-section"></a>Nesta seção

[Iniciar sessão MAPI](starting-a-mapi-session.md)
  
> Descreve como iniciar uma sessão MAPI e inclui links para tópicos com informações mais detalhadas.
    
[Finalizar uma sessão MAPI](ending-a-mapi-session.md)
  
> Descreve como encerrar uma sessão MAPI.
    
[Acessar objetos usando a sessão](accessing-objects-by-using-the-session.md)
  
> Descreve como usar um ponteiro de sessão para acessar objetos de sessão.
    
[Recuperar identidade principal e do provedor](retrieving-primary-and-provider-identity.md)
  
> Descreve as propriedades usadas para recuperar primário e a identidade do provedor.
    
[Tabela de status e objetos de status](status-table-and-status-objects.md)
  
> Descreve como acessar as informações da tabela de status.
    

