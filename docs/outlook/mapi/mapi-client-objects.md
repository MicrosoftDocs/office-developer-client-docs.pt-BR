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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319283"
---
# <a name="mapi-client-objects"></a>Objetos de cliente MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos clientes de mensagens padrão implementam apenas um objeto — um coletor de aviso. Os coletores de aviso herdam da interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) e são usados por MAPI e provedores de serviço para notificação de eventos. Alguns clientes também implementam objetos Progress para dar suporte à exibição de caixas de diálogo de progresso. 
  
Clientes mais complexos que oferecem suporte a formulários personalizados implementam outro objeto de coletor de aviso e alguns outros objetos, como o objeto de site de mensagem que herda da interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) e o objeto de contexto de exibição que herda da [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) interface. O objeto de coletor de aviso adicional herda da interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) . 
  
A tabela a seguir resume os objetos MAPI implementados por clientes de mensagens padrão e por clientes que dão suporte à exibição de formulários personalizados.
  
|**Objeto Client**|**Descrição**|
|:-----|:-----|
|Coletor de aviso  <br/> |Fornece uma função de retorno de chamada para eventos que ocorrem no repositório de mensagens, no catálogo de endereços ou na sessão.  <br/> |
|Site de mensagens  <br/> |Manipula a manipulação de objetos Form.  <br/> |
|Progress  <br/> |Exibe uma caixa de diálogo para mostrar o progresso de uma operação.  <br/> |
|Exibir coletor de avisos  <br/> |Fornece funções de retorno de chamada para eventos que ocorrem em um formulário.  <br/> |
|Contexto de exibição  <br/> |Suporta comandos para imprimir e salvar formulários e para navegar entre formulários.  <br/> |
   
A ilustração a seguir mostra a relação entre esses objetos cliente diferentes, as interfaces das quais eles herdam e os componentes MAPI que os utilizam. 
  
![Objetos de cliente e interfaces correspondentes] (media/amapi_65.gif "Objetos de cliente e interfaces correspondentes")
  
Os clientes usam muitos outros objetos do que eles implementam. Todos os clientes usam um objeto Session para obter acesso a uma ampla variedade de objetos de provedor de serviços e objetos que o MAPI implementa. Os clientes interagem com os provedores de serviço indiretamente, através da sessão, do catálogo de endereços ou dos objetos de status que o MAPI fornece ou diretamente por uma variedade de objetos implementados por provedores de serviços específicos. Para fazer contato direto com provedores de catálogo de endereços, os clientes usam contêineres de catálogo de endereços, usuários de mensagens e listas de distribuição. Para acessar diretamente um provedor de armazenamento de mensagens, os clientes usam o objeto, as pastas, as mensagens e os anexos do repositório de mensagens. Quando os provedores de serviços dão suporte a um objeto status, os clientes podem usar o objeto status para monitorar o estado do provedor de serviços.
  
Os clientes que dão suporte ao provedor de serviços e à configuração do serviço de mensagens usam três objetos que o MAPI implementa: o objeto de administração do serviço de mensagens, o objeto de administração de perfil e o objeto de administração de provedor Os clientes que exibem formulários personalizados usam vários objetos de formulário que um provedor de biblioteca de formulários ou um servidor de formulários implementa.
  
## <a name="see-also"></a>Confira também

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [Visão geral de interface e objeto MAPI](mapi-object-and-interface-overview.md)

