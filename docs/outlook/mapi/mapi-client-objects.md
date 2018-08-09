---
title: Objetos de cliente MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fb37c15e6544798a956e865e6c8c6d62bee44d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767834"
---
# <a name="mapi-client-objects"></a>Objetos de cliente MAPI
  
**Aplica-se a**: Outlook 
  
Aplicativos de cliente de mensagens padrão implementam apenas um objeto — um coletor advise. Avise PIAs herdem a [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interface e são usados pelo MAPI e provedores de notificação de evento de serviço. Alguns clientes também implementam objetos de andamento para oferecer suporte a exibição das caixas de diálogo de progresso. 
  
Coletor de clientes mais complexos que formulários personalizados do suporte implementam advise outro objeto e alguns outros objetos, tais como o objeto de site de mensagem que herde a [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interface e o objeto de contexto do modo de exibição que herda do [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) interface. O objeto coletor de eventos adicionais advise herde a [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interface. 
  
A tabela a seguir resume os objetos MAPI implementados por clientes de mensagens padrão e por clientes que oferecem suporte à exibição de formulários personalizados.
  
|**Objeto de cliente**|**Descrição**|
|:-----|:-----|
|Coletor de eventos de aviso  <br/> |Fornece uma função de retorno de chamada para eventos que ocorrem no armazenamento de mensagens, catálogo de endereços ou a sessão.  <br/> |
|Site de mensagem  <br/> |Trata a manipulação de objetos de formulário.  <br/> |
|Progress  <br/> |Exibe uma caixa de diálogo para mostrar o progresso de uma operação.  <br/> |
|Coletor de eventos de aviso do modo de exibição  <br/> |Fornece funções de retorno de chamada para eventos que ocorrem em um formulário.  <br/> |
|Contexto de modo de exibição  <br/> |Oferece suporte a comandos para impressão e salvamento de formulários e navegação entre formulários.  <br/> |
   
A ilustração a seguir mostra a relação entre esses objetos de cliente diferente, as interfaces do qual eles herdam e os componentes MAPI que usá-los. 
  
![Objetos de cliente e as interfaces correspondentes] (media/amapi_65.gif "Objetos de cliente e as interfaces correspondentes")
  
Os clientes usam muitos mais objetos do que eles implementam. Todos os clientes usam um objeto de sessão para obter acesso a uma ampla variedade de objetos do provedor de serviço e objetos que implementa MAPI. Os clientes interagem com provedores de serviços indiretamente, através da sessão, o catálogo de endereços ou os objetos de status que fornece MAPI ou diretamente por meio de uma variedade de objetos que implementam provedores de serviço específico. Para tornar o contato direto com provedores de catálogo de endereços, os clientes usam os contêineres do catálogo de endereços, usuários e listas de distribuição de mensagens. Para acessar um provedor de armazenamento de mensagem diretamente, os clientes usam o objeto de armazenamento de mensagens, pastas, mensagens e anexos. Quando os provedores de serviço oferecem suporte a um objeto de status, os clientes podem usar o objeto de status para monitorar o estado do provedor de serviços.
  
Clientes com suporte do provedor de serviços e a configuração do serviço de mensagem usam três objetos que implementa MAPI: o objeto de administração do serviço de mensagem, o objeto de administração do perfil e o objeto de administração do provedor. Os clientes que exibem os formulários personalizados usam vários objetos de formulário que implementa um provedor de biblioteca de formulário ou um servidor de formulário.
  
## <a name="see-also"></a>Confira também

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

