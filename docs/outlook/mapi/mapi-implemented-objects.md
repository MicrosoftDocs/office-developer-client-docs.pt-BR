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
  
O MAPI implementa vários objetos para uso por aplicativos cliente e provedores de serviços. O objeto session permite que os clientes usem serviços de sessão, acessem tabelas e se comuniquem com provedores de serviços. O objeto de livro de endereços fornece aos clientes acesso integrado a todos os diferentes provedores de agendas. 
  
O MAPI fornece vários objetos de tabela e status para os clientes usarem para exibir e monitorar informações de sessão e provedor de serviços. Por exemplo, o MAPI fornece uma tabela de perfil com informações sobre todos os perfis instalados no computador e uma tabela de serviço de mensagens com informações sobre todos os serviços de mensagem no perfil atual. MAPI provides three different status objects: one that represents the overall subsystem, one for the MAPI spooler, and one for the integrated address book. 
  
O MAPI implementa quatro objetos diferentes para gerenciar a configuração de serviços de mensagens, provedores de serviços e perfis. Clientes e provedores de serviços usam objetos de seção de perfil e administração de provedor; esses objetos permitem que eles configurem provedores de serviços e acessem propriedades de perfil. Os clientes usam apenas objetos de administração de perfil e serviço de mensagens, os objetos que suportam a administração de perfis e serviços de mensagens. 
  
O MAPI fornece dois objetos para provedores de serviços: um objeto de suporte e um objeto TNEF. Todos os provedores de serviços usam um ou mais objetos de suporte; há quatro implementações de objeto de suporte diferentes. O MAPI fornece uma implementação para dar suporte à configuração, bem como implementações específicas para dar suporte ao address book, ao armazenamento de mensagens e aos provedores de transporte. O objeto TNEF é usado por provedores de transporte que suportam o TNEF (Transport Neutral Encapsulation Format).
  
Dois objetos utilitários, dados de tabela e dados de propriedade, são geralmente usados por provedores de serviços. Objetos de dados de tabela ajudam na implementação de objetos de tabela; objetos de dados de propriedade ajudam a definir e exibir o acesso à propriedade e ajudam na implementação de [IMAPIProp : IUnknown](imapipropiunknown.md), a interface de propriedade base. 
  
A tabela a seguir resume a finalidade de cada objeto que o MAPI implementa.
  
|**Objeto MAPI**|**Descrição**|
|:-----|:-----|
|Catálogo de endereços  <br/> |Fornece acesso à exibição integrada das informações do destinatário que pertence a todos os provedores de agenda do perfil ativo.  <br/> |
|Administração do serviço de mensagens  <br/> |Fornece acesso às informações do serviço de mensagens para configuração.  <br/> |
|Administração de perfil  <br/> |Fornece acesso às informações de perfil para configuração.  <br/> |
|Seção Profile  <br/> |Uma parte de um perfil usado para descrever um determinado serviço de mensagens ou provedor de serviços.  <br/> |
|Dados de propriedade  <br/> |Mantém o acesso às propriedades e ajuda a implementar **IMAPIProp**.  <br/> |
|Administração do provedor  <br/> |Fornece acesso às informações do provedor de serviços para configuração.  <br/> |
|Sessão  <br/> |Representa uma conexão com sistemas de mensagens subjacentes e fornece aos clientes acesso aos recursos MAPI.  <br/> |
|Status  <br/> |Fornece acesso ao estado do subsistema MAPI, do livro de endereços ou do spooler MAPI.  <br/> |
|Suporte  <br/> |Ajuda os provedores de serviços a lidar com solicitações de clientes.  <br/> |
|Table  <br/> |Fornece acesso a uma exibição resumida de dados de objeto no formato de linha e coluna, semelhante a uma tabela de banco de dados.  <br/> |
|Dados de tabela  <br/> |Mantém o acesso aos dados da tabela subjacente e implementa objetos de tabela.  <br/> |
|TNEF  <br/> |Dá suporte ao uso do TNEF (Transport Neutral Encapsulation Format).  <br/> |
   
A ilustração a seguir mostra a relação entre os objetos que o MAPI implementa, as interfaces das quais eles herdam e os componentes que os utilizam. 
  
**Objects that MAPI implements**
  
![Objetos que o MAPI implementa](media/amapi_68.gif "objetos que o MAPI implementa")
  
## <a name="see-also"></a>Confira também

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Visão geral de objetos e interface MAPI](mapi-object-and-interface-overview.md)

