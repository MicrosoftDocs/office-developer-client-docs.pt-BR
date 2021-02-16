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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432265"
---
# <a name="mapi-service-provider-objects"></a>Objetos do provedor de serviços MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de serviços implementam muitos objetos. Algumas são usadas principalmente por MAPI e outras são usadas por aplicativos cliente. Alguns objetos são implementados por todos os tipos de provedores de serviços; o restante é específico para um único tipo de provedor. A tabela a seguir descreve todos os objetos do provedor de serviços.
  
|**Objeto do provedor de serviços**|**Descrição**|
|:-----|:-----|
|Contêiner do livro de endereços  <br/> |Contém informações de destinatário para um provedor de livro de endereços no perfil ativo; os provedores de agenda podem ter um ou mais contêineres de livro de endereços.  <br/> |
|Anexo  <br/> |Contém dados adicionais, como um arquivo ou objeto OLE, a serem associados a uma mensagem.  <br/> |
|Controle  <br/> |Habilita ou desabilita um botão e inicia o processamento quando o botão é clicado.  <br/> |
|Lista de distribuição  <br/> |Descreve um grupo de destinatários de mensagens individuais.  <br/> |
|Folder  <br/> |Contém mensagens e outros contêineres de mensagens.  <br/> |
|Logon  <br/> |Lida com a notificação de evento do provedor de serviços e as solicitações de cliente.  <br/> |
|Usuário de mensagens  <br/> |Descreve um destinatário individual de uma mensagem.  <br/> |
|Mensagem  <br/> |Contém informações que podem ser enviadas a um ou mais destinatários.  <br/> |
|Armazenamento de mensagens  <br/> |Atua como um banco de dados hierárquico de mensagens.  <br/> |
|Provedor  <br/> |Lida com a inicialização e o desligamento do provedor de serviços.  <br/> |
|Spooler hook  <br/> |Executa processamento especial em mensagens de entrada e saída.  <br/> |
|Status  <br/> |Fornece acesso ao estado do provedor de serviços.  <br/> |
|Table  <br/> |Fornece acesso a uma exibição resumida de dados de objeto no formato de linha e coluna, semelhante a uma tabela de banco de dados.  <br/> |
   
Todos os provedores de serviços implementam um objeto de provedor e um objeto de logon. Os objetos de provedor são estritamente para a manutenção contábil; eles são usados pelo MAPI para controlar os processos de inicialização e desligamento. Os objetos de logon a serviço de algumas solicitações de cliente indiretamente. Por exemplo, o objeto de logon do provedor de armazenamento de mensagens lida com o registro de notificação e solicitações para abrir objetos do armazenamento de mensagens. 
  
Os objetos de provedor e logon implementam uma interface diferente, dependendo do tipo de provedor de serviços que fornece a implementação. Um provedor de armazenamento de mensagens implementa o [IMSProvider : IUnknown](imsprovideriunknown.md) e [IMSLogon : interfaces IUnknown](imslogoniunknown.md) em seu provedor e objetos de logon, um provedor de agendamento implementa o [IABProvider : IUnknown](iabprovideriunknown.md) e [IABLogon : interfaces IUnknown](iablogoniunknown.md) e um provedor de transporte implementa [o IXPProvider : IUnknown](ixpprovideriunknown.md) e [IXPLogon : interfaces IUnknown.](ixplogoniunknown.md) 
  
Provedores de gancho de mensagem implementam objetos de gancho de spooler ou objetos que filtram mensagens de entrada e saída.
  
Os provedores de serviços normalmente usam apenas alguns objetos. Com mais frequência, eles usam um objeto de suporte que o MAPI fornece para ajudar a implementar solicitações de cliente. O objeto de suporte é personalizado para o tipo de provedor que o está usando. Para todos os provedores de serviços, o objeto de suporte inclui métodos para manipular a notificação de eventos, exibir propriedades de configuração, abrir objetos e tratamento de erros. O restante dos métodos são específicos para seu uso; há versões personalizadas para o livro de endereços, o armazenamento de mensagens e os provedores de transporte e para suporte à configuração. Por exemplo, o objeto de suporte do livro de endereços exibe detalhes e caixas de diálogo de destinatário personalizadas. O objeto de suporte do armazenamento de mensagens oferece suporte a operações de copiar e mover para pastas e mensagens. O objeto de suporte do provedor de transporte inclui métodos para facilitar a interação com o spooler MAPI. 
  
Alguns provedores de serviços usam dados de tabela e objetos de dados de propriedade — objetos utilitários que o MAPI implementa. Os objetos de dados de tabela permitem que os provedores de serviços gerenciem os dados subjacentes de uma tabela. Objetos de dados de propriedade permitem que provedores de serviços de definir o acesso a objetos e propriedades. 
  
Provedores de transporte que suportam o TNEF (Transport Neutral Encapsulation Format) para transferir propriedades usam um objeto TNEF que o MAPI implementa para dar suporte à interface [ITnef : IUnknown.](itnefiunknown.md) Para obter mais informações, [consulte Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Confira também



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Desenvolvendo um provedor TNEF-Enabled transporte de conteúdo](developing-a-tnef-enabled-transport-provider.md)

