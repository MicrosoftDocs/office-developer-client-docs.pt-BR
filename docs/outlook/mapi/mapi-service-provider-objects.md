---
title: Objetos do provedor de serviço MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 505b27b469a4ab197b41058ea5b933608818f0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767936"
---
# <a name="mapi-service-provider-objects"></a>Objetos do provedor de serviço MAPI

  
  
**Aplica-se a**: Outlook 
  
Provedores de serviço implementar vários objetos. Alguns são usados principalmente pelos MAPI e alguns são usados por aplicativos do cliente. Alguns objetos são implementados por todos os tipos de provedores de serviços; o restante são específicos para um tipo de provedor único. A tabela a seguir descreve todos os objetos do provedor de serviço.
  
|**Objeto de provedor de serviço**|**Descrição**|
|:-----|:-----|
|Contêiner de catálogo de endereços  <br/> |Contém informações de destinatário para um provedor de catálogo de endereços no perfil ativo; provedores de catálogo de endereços podem ter um ou mais contêineres do catálogo de endereços.  <br/> |
|Anexo  <br/> |Contém dados adicionais, como um arquivo ou objeto OLE, a ser associado uma mensagem.  <br/> |
|Control  <br/> |Habilita ou desabilita um botão e inicia o processamento quando o botão é clicado.  <br/> |
|Lista de distribuição  <br/> |Descreve um agrupamento de destinatários da mensagem individuais.  <br/> |
|Folder  <br/> |Contém mensagens e outros contêineres de mensagem.  <br/> |
|Logon  <br/> |As alças de solicitações de notificação e cliente de evento de provedor de serviço.  <br/> |
|Usuário de mensagens  <br/> |Descreve um destinatário individual de uma mensagem.  <br/> |
|Message  <br/> |Contém informações que podem ser enviadas para um ou mais destinatários.  <br/> |
|Armazenamento de mensagens  <br/> |Atua como um banco de dados organizado hierarquicamente das mensagens.  <br/> |
|Provider  <br/> |As alças de desligamento e inicialização do provedor de serviço.  <br/> |
|Gancho spooler  <br/> |Realiza processamento especial em mensagens de entrada e saídas.  <br/> |
|Status  <br/> |Fornece acesso ao estado do provedor de serviços.  <br/> |
|Table  <br/> |Fornece acesso a um modo de exibição de resumo de dados de objeto no formato de linha e coluna, semelhante a uma tabela de banco de dados.  <br/> |
   
Todos os provedores de serviço implementam um objeto do provedor e um objeto de logon. Objetos do provedor são estritamente para escrituração contábil; eles são usados pelo MAPI para controlar os processos de inicialização e desligamento. Objetos de logon do serviço indiretamente algumas solicitações de cliente. Por exemplo, a mensagem armazenar solicitações para abrir objetos do repositório de mensagem e o registro de notificação alças do objeto de logon do provedor. 
  
Objetos de provedor e logon implementar uma interface diferente, dependendo do tipo de provedor de serviço que fornece a implementação. Implementa um provedor de armazenamento de mensagem do [IMSProvider: IUnknown](imsprovideriunknown.md) e [IMSLogon: IUnknown](imslogoniunknown.md) interfaces no seu provedor e objetos de logon, um endereço livro provedor implementa o [IABProvider: IUnknown](iabprovideriunknown.md) e [IABLogon: IUnknown](iablogoniunknown.md) interfaces e um provedor de transporte implementa o [IXPProvider: IUnknown](ixpprovideriunknown.md) e [IXPLogon: IUnknown](ixplogoniunknown.md) interfaces. 
  
Provedores de fora do gancho de mensagem implementar objetos de fora do gancho spooler ou objetos que filtrar mensagens de entrada e saídas.
  
Provedores de serviço geralmente usam apenas alguns objetos. Com mais frequência, eles usam um objeto de suporte a MAPI fornece para ajudar a implementar as solicitações do cliente. O objeto de suporte é personalizado para o tipo de provedor que está sendo usada. Para todos os provedores de serviço, o objeto de suporte inclui métodos para manipulação de notificação de evento, exibindo as propriedades de configuração, os objetos de abertura e tratamento de erros. O restante dos métodos são específicos para o seu uso; Há versões personalizadas para o catálogo de endereços, armazenamento de mensagens e provedores de transporte e para suporte de configuração. Por exemplo, o objeto de suporte de catálogo de endereços exibe detalhes e caixas de diálogo personalizadas de destinatário. O armazenamento de mensagens oferecem suporte a cópia do objeto suporta e mover as operações para mensagens e pastas. O objeto de suporte do provedor de transporte inclui métodos para facilitar a interação com o spooler MAPI. 
  
Alguns provedores de serviço usam objetos de dados de dados e a propriedade table — objetos utilitário que implementa de MAPI. Objetos de dados de tabela habilite provedores de serviços gerenciar os dados subjacentes de uma tabela. Objetos de dados de propriedade habilite provedores de serviço definir o acesso do objeto e a propriedade. 
  
Provedores de transporte que suportam o TNEF Transport Neutral Encapsulation Format () para transferir propriedades usam um objeto TNEF que implementa de MAPI para oferecer suporte a [ITnef: IUnknown](itnefiunknown.md) interface. Para obter mais informações, consulte [desenvolvendo um provedor de transporte TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Confira também



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Desenvolver um provedor de transporte habilitado por TNEF](developing-a-tnef-enabled-transport-provider.md)

