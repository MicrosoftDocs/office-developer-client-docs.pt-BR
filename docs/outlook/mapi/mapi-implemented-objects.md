---
title: Objetos implementados por MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 86aa8451b5b127764134f1a3a905366fd014d0c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430627"
---
# <a name="mapi-implemented-objects"></a>Objetos implementados por MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI implementa vários objetos para uso por aplicativos cliente e provedores de serviço. O objeto Session permite que os clientes usem serviços de sessão, acessem tabelas e se comuniquem com provedores de serviços. O objeto catálogo de endereços fornece aos clientes acesso integrado a todos os diferentes provedores de catálogo de endereços. 
  
O MAPI fornece vários objetos table e status para os clientes usarem para exibir e monitorar as informações de sessão e provedor de serviços. Por exemplo, o MAPI fornece uma tabela de perfil com informações sobre todos os perfis instalados no computador e uma tabela de serviço de mensagens com informações sobre todos os serviços de mensagens no perfil atual. MAPI fornece três objetos de status diferentes: um que representa o subsistema geral, um para o spooler MAPI e um para o catálogo de endereços integrado. 
  
O MAPI implementa quatro objetos diferentes para gerenciar a configuração de serviços de mensagens, provedores de serviços e perfis. Os clientes e provedores de serviços usam a administração do provedor e os objetos da seção de perfil; esses objetos permitem que eles configurem provedores de serviço e propriedades de perfil de acesso. Os clientes usam somente objetos de serviço de mensagens e de administração de perfil, os objetos que oferecem suporte à administração de serviços e perfis de mensagem. 
  
MAPI fornece dois objetos para provedores de serviço: um objeto support e um objeto TNEF. Todos os provedores de serviços usam um ou mais objetos de suporte; Há quatro implementações de objetos de suporte diferentes. O MAPI fornece uma implementação para suportar a configuração, bem como implementações específicas para suportar o catálogo de endereços, o repositório de mensagens e os provedores de transporte. O objeto TNEF é usado por provedores de transporte que dão suporte ao protocolo TNEF (Transport neutral Encapsulation Format).
  
Dois objetos utilitários, dados de tabela e dados de propriedade, geralmente são usados por provedores de serviços. Os objetos de dados da tabela ajudam na implementação de objetos table; os objetos de dados de propriedade ajudam a definir e exibir o acesso de propriedade e a ajuda na implementação de [IMAPIProp: IUnknown](imapipropiunknown.md), a interface de propriedade básica. 
  
A tabela a seguir resume a finalidade de cada objeto que a MAPI implementa.
  
|**Objeto MAPI**|**Descrição**|
|:-----|:-----|
|Catálogo de endereços  <br/> |Fornece acesso à exibição integrada de informações de destinatário que pertencem a todos os provedores de catálogo de endereços no perfil ativo.  <br/> |
|Administração do serviço de mensagens  <br/> |Fornece acesso às informações do serviço de mensagens para configuração.  <br/> |
|Administração de perfis  <br/> |Fornece acesso a informações de perfil para configuração.  <br/> |
|Seção Profile  <br/> |Uma parte de um perfil usado para descrever um determinado serviço de mensagens ou provedor de serviços.  <br/> |
|Dados de propriedade  <br/> |Mantém o acesso às propriedades e ajuda a implementar o **IMAPIProp**.  <br/> |
|Administração de provedor  <br/> |Fornece acesso a informações do provedor de serviços para configuração.  <br/> |
|Sessão  <br/> |Representa uma conexão com sistemas de mensagens subjacentes e fornece aos clientes acesso a recursos MAPI.  <br/> |
|Status  <br/> |Fornece acesso ao estado do subsistema MAPI, do catálogo de endereços ou do spooler MAPI.  <br/> |
|Suporte  <br/> |Ajuda os provedores de serviços a lidar com as solicitações do cliente.  <br/> |
|Tabela  <br/> |Fornece acesso a um modo de exibição de resumo dos dados de objeto em formato de linha e coluna, semelhante a uma tabela de banco de dados.  <br/> |
|Dados de tabela  <br/> |Mantém o acesso aos dados da tabela base e implementa os objetos table.  <br/> |
|TNEF  <br/> |Dá suporte ao uso do formato de encapsulamento neutro de transporte (TNEF).  <br/> |
   
A ilustração a seguir mostra a relação entre os objetos que o MAPI implementa, as interfaces das quais eles herdam e os componentes que os utilizam. 
  
**Objects that MAPI implements**
  
![Objetos que o MAPI implementa] (media/amapi_68.gif "Objetos que o MAPI implementa")
  
## <a name="see-also"></a>Confira também

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Visão geral de interface e objeto MAPI](mapi-object-and-interface-overview.md)

