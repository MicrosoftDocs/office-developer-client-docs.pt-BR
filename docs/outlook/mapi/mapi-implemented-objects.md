---
title: Objetos implementada de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d212a86aae0503a5e02a5a7ecddb83db10a4d664
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572372"
---
# <a name="mapi-implemented-objects"></a>Objetos implementada de MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI implementa vários objetos para uso por provedores de serviços e aplicativos cliente. O objeto de sessão permite aos clientes utilizarem serviços de sessão, para acessar tabelas e se comuniquem com provedores de serviço. O objeto de catálogo de endereços fornece clientes com acesso integrado para todos os provedores de catálogo de endereço diferente. 
  
MAPI fornece vários objetos de tabela e status para clientes usarem para exibição e informações do provedor de sessão e o serviço de monitoramento. Por exemplo, MAPI fornece uma tabela de perfil com informações sobre todos os perfis que estão instalados no computador e uma tabela de serviço de mensagem com informações sobre todos os serviços de mensagem no perfil atual. MAPI fornece três objetos diferentes status: uma que representa o subsistema de geral, um para o spooler MAPI e outro para o catálogo de endereços integrada. 
  
MAPI implementa quatro objetos diferentes para gerenciar a configuração de serviços de mensagens, provedores de serviços e perfis. Provedores de serviços e clientes usam a administração do provedor e objetos de seção perfil; Esses objetos habilitá-los configurar provedores de serviços e acessar propriedades de perfil. Os clientes usam apenas o serviço de mensagem e objetos de administração de perfil, os objetos que permitem a administração dos serviços de mensagem e perfis. 
  
MAPI fornece dois objetos para provedores de serviço: um objeto de suporte e um objeto TNEF. Todos os provedores de serviços usam um ou mais objetos de suporte; Há quatro implementações de objeto de suporte de diferentes. MAPI fornece uma implementação para oferecer suporte a configuração, bem como implementações específicas para dar suporte ao catálogo de endereços, armazenamento de mensagens e provedores de transporte. O objeto TNEF é usado pelos provedores de transporte que suportam o TNEF Transport Neutral Encapsulation Format ().
  
Dois objetos utilitário, dados da tabela e dados de propriedade, geralmente são usados pelos provedores de serviços. Objetos de dados de tabela ajudam na implementação de objetos table; Ajuda de objetos de dados de propriedade para o acesso à propriedade definido e o modo de exibição e ajuda na implementação do [IMAPIProp: IUnknown](imapipropiunknown.md), a interface de propriedade base. 
  
A tabela a seguir resume o objetivo de cada objeto que implementa de MAPI.
  
|**Objeto MAPI**|**Descrição**|
|:-----|:-----|
|Catálogo de endereços  <br/> |Fornece acesso ao modo de exibição integrado de informações do destinatário que pertence a todos os provedores de catálogo de endereços no perfil atual.  <br/> |
|Administração do serviço de mensagem  <br/> |Fornece acesso a informações de serviço de mensagem para a configuração.  <br/> |
|Administração de perfil  <br/> |Fornece acesso às informações de perfil de configuração.  <br/> |
|Seção de perfil  <br/> |Uma parte de um perfil usado para descrever um serviço de mensagem específica ou de um provedor de serviços.  <br/> |
|Dados de propriedade  <br/> |Mantém o acesso às propriedades e ajuda a implementar **IMAPIProp**.  <br/> |
|Administração do provedor  <br/> |Oferece acesso a informações do provedor de serviço de configuração.  <br/> |
|Sessão  <br/> |Representa uma conexão aos sistemas de mensagens subjacentes e fornece aos clientes acesso aos recursos MAPI.  <br/> |
|Status  <br/> |Fornece acesso ao estado do subsistema de MAPI, o catálogo de endereços ou o spooler MAPI.  <br/> |
|Suporte  <br/> |Ajuda a provedores de serviços de lidar com as solicitações do cliente.  <br/> |
|Table  <br/> |Fornece acesso a um modo de exibição de resumo de dados de objeto no formato de linha e coluna, semelhante a uma tabela de banco de dados.  <br/> |
|Dados da tabela  <br/> |Mantém o acesso a dados de tabela base e implementa objetos table.  <br/> |
|TNEF  <br/> |Suporta o uso do TNEF Transport Neutral Encapsulation Format ().  <br/> |
   
A ilustração a seguir mostra a relação entre os objetos que implementa MAPI, as interfaces do qual eles herdam e os componentes que usá-los. 
  
**Objects that MAPI implements**
  
![Objetos que implementa MAPI] (media/amapi_68.gif "Objetos que implementa MAPI")
  
## <a name="see-also"></a>Confira também

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Objeto MAPI e visão geral da Interface](mapi-object-and-interface-overview.md)

