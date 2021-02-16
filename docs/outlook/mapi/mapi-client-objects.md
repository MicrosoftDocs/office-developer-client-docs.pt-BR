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
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412405"
---
# <a name="mapi-client-objects"></a>Objetos de cliente MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplicativos cliente de mensagens padrão implementam apenas um objeto — um evento de aconselhá-los. Os sinks de aviso herdam da interface [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) e são usados por MAPI e provedores de serviços para notificação de eventos. Alguns clientes também implementam objetos de progresso para dar suporte à exibição de caixas de diálogo de progresso. 
  
Clientes mais complexos que suportam formulários personalizados implementam outro objeto sink de consultoria e alguns outros objetos, como o objeto de site de mensagem que herda da interface [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) e o objeto de contexto de exibição que herda do [IMAPIViewContext : interface IUnknown.](imapiviewcontextiunknown.md) O objeto sink de atribuição adicional herda da [interface IMAPIViewAdviseSink : IUnknown.](imapiviewadvisesinkiunknown.md) 
  
A tabela a seguir resume os objetos MAPI implementados por clientes de mensagens padrão e por clientes que suportam a exibição de formulários personalizados.
  
|**Objeto Client**|**Descrição**|
|:-----|:-----|
|Aconselhá-o  <br/> |Fornece uma função de retorno de chamada para eventos que ocorrem no armazenamento de mensagens, no address book ou na sessão.  <br/> |
|Site de mensagens  <br/> |Manipula a manipulação de objetos de formulário.  <br/> |
|Progress  <br/> |Exibe uma caixa de diálogo para mostrar o progresso de uma operação.  <br/> |
|View advise sink  <br/> |Fornece funções de retorno de chamada para eventos que ocorrem em um formulário.  <br/> |
|Exibir contexto  <br/> |Oferece suporte a comandos para imprimir e salvar formulários e para navegar entre formulários.  <br/> |
   
A ilustração a seguir mostra a relação entre esses diferentes objetos de cliente, as interfaces das quais eles herdam e os componentes MAPI que os utilizam. 
  
![Objetos cliente e interfaces correspondentes](media/amapi_65.gif "Objetos cliente e interfaces correspondentes")
  
Os clientes usam muito mais objetos do que implementam. Todos os clientes usam um objeto session para obter acesso a uma ampla variedade de objetos e objetos do provedor de serviços que o MAPI implementa. Os clientes interagem com provedores de serviços indiretamente, por meio da sessão, do livro de endereços ou dos objetos de status que o MAPI fornece, ou diretamente por meio de uma variedade de objetos implementados por determinados provedores de serviços. Para fazer contato direto com provedores de listas de endereços, os clientes usam contêineres de listas de endereços, usuários de mensagens e listas de distribuição. Para acessar um provedor de armazenamento de mensagens diretamente, os clientes usam o objeto, pastas, mensagens e anexos do armazenamento de mensagens. Quando os provedores de serviços suportam um objeto de status, os clientes podem usar o objeto de status para monitorar o estado do provedor de serviços.
  
Os clientes que suportam a configuração do provedor de serviços e do serviço de mensagens usam três objetos que o MAPI implementa: o objeto de administração do serviço de mensagens, o objeto de administração de perfil e o objeto de administração do provedor. Os clientes que exibem formulários personalizados usam vários objetos de formulário implementados por um provedor de biblioteca de formulários ou por um servidor de formulários.
  
## <a name="see-also"></a>Confira também

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Visão geral de objetos e interface MAPI](mapi-object-and-interface-overview.md)

