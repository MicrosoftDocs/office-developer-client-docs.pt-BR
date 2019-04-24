---
title: Objetos do provedor de serviços MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0976e986a33d8b96366a84527f227bd05ef7845e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251602"
---
# <a name="mapi-service-provider-objects"></a>Objetos do provedor de serviços MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de serviços implementam muitos objetos. Alguns são usados principalmente por MAPI e outros são usados por aplicativos cliente. Alguns objetos são implementados por todos os tipos de provedores de serviços; o REST é específico para um único tipo de provedor. A tabela a seguir descreve todos os objetos do provedor de serviços.
  
|**Objeto provedor de serviços**|**Descrição**|
|:-----|:-----|
|Contêiner de catálogo de endereços  <br/> |Contém informações de destinatário para um provedor de catálogo de endereços no perfil ativo; os provedores de catálogo de endereços podem ter um ou mais contêineres de catálogo de endereços.  <br/> |
|Anexo  <br/> |Contém dados adicionais, como um arquivo ou objeto OLE, a serem associados a uma mensagem.  <br/> |
|Control  <br/> |Habilita ou desabilita um botão e inicia o processamento quando o botão é clicado.  <br/> |
|Lista de distribuição  <br/> |Descreve um agrupamento de destinatários de mensagens individuais.  <br/> |
|Pasta  <br/> |Contém mensagens e outros contêineres de mensagem.  <br/> |
|Logon  <br/> |Manipula as solicitações de eventos do provedor de serviços e as solicitações do cliente.  <br/> |
|Usuário de mensagens  <br/> |Descreve um destinatário individual de uma mensagem.  <br/> |
|Mensagem  <br/> |Contém informações que podem ser enviadas para um ou mais destinatários.  <br/> |
|Repositório de mensagens  <br/> |Atua como um banco de dados de mensagens hierarquicamente organizado.  <br/> |
|Provedor  <br/> |Manipula a inicialização e o desligamento do provedor de serviço.  <br/> |
|Conexão de spooler  <br/> |Realiza processamento especial em mensagens de entrada e saída.  <br/> |
|Status  <br/> |Fornece acesso ao estado do provedor de serviços.  <br/> |
|Tabela  <br/> |Fornece acesso a um modo de exibição de resumo dos dados de objeto em formato de linha e coluna, semelhante a uma tabela de banco de dados.  <br/> |
   
Todos os provedores de serviços implementam um objeto de provedor e um objeto de logon. Os objetos Provider são estritamente para escrituração de contador; Eles são usados pelo MAPI para controlar os processos de inicialização e desligamento. O serviço de objetos de logon algumas solicitações de clientes indiretamente. Por exemplo, o objeto de logon do provedor de repositório de mensagens manipula o registro de notificação e as solicitações para abrir objetos do repositório de mensagens. 
  
Os objetos Provider e logon implementam uma interface diferente dependendo do tipo de provedor de serviço que fornece a implementação. Um provedor de repositório de mensagens implementa as interfaces [IMSProvider: IUnknown](imsprovideriunknown.md) e [IMSLogon: IUnknown](imslogoniunknown.md) em seus objetos Provider e login, um provedor de catálogo de endereços implementa o [IABProvider: IUnknown](iabprovideriunknown.md) e [IABLogon: IUnknown](iablogoniunknown.md) interfaces, e um provedor de transporte implementa as interfaces [IXPProvider: IUnknown](ixpprovideriunknown.md) e [IXPLogon: IUnknown](ixplogoniunknown.md) . 
  
Os provedores de conexão de mensagens implementam objetos de conexão do spooler ou objetos que filtram mensagens de entrada e saída.
  
Os provedores de serviços normalmente usam apenas alguns objetos. Com mais frequência, eles usam um objeto de suporte que o MAPI fornece para ajudar a implementar as solicitações do cliente. O objeto support é personalizado para o tipo de provedor que o está usando. Para todos os provedores de serviços, o objeto support inclui métodos para manipular a notificação de eventos, exibir propriedades de configuração, abrir objetos e tratamento de erros. O restante dos métodos é específico para seu uso; Há versões personalizadas para o catálogo de endereços, o repositório de mensagens e os provedores de transporte e para o suporte à configuração. Por exemplo, o objeto de suporte do catálogo de endereços exibe as caixas de diálogo detalhes e destinatário personalizado. O objeto de suporte do repositório de mensagens oferece suporte a operações de cópia e movimentação para pastas e mensagens. O objeto de suporte do provedor de transporte inclui métodos para facilitar a interação com o spooler MAPI. 
  
Alguns provedores de serviços usam dados de tabela e objetos de dados de propriedade — objetos utilitários que o MAPI implementa. Os objetos de dados de tabela permitem que os provedores de serviços gerenciem os dados subjacentes de uma tabela. Os objetos de dados de propriedade permitem que os provedores de serviços definam acesso de objeto e propriedade. 
  
Os provedores de transporte que oferecem suporte ao formato de encapsulamento de transporte neutro (TNEF) para a transferência de Propriedades usam um objeto TNEF que o MAPI implementa para dar suporte à interface [ITnef: IUnknown](itnefiunknown.md) . Para obter mais informações, consulte [desenvolvimento de um provedor de transporte habilitado para TNEF](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Confira também



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Desenvolver um provedor de transporte habilitado para TNEF](developing-a-tnef-enabled-transport-provider.md)

