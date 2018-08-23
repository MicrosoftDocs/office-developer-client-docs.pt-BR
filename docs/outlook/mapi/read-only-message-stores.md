---
title: Repositórios de mensagens somente leitura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 752ff2d6-ca64-4507-adf1-4c054c321203
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e0a66443194a3f89b47218ed9dc0ed9ad9c2df83
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584510"
---
# <a name="read-only-message-stores"></a>Repositórios de mensagens somente leitura

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um armazenamento de mensagens de somente leitura é uma nos quais não o cliente MAPI nem o MAPI spooler pode criar, modificar ou excluir os objetos no repositório de mensagem. Há vários motivos por que talvez você queira implementar um armazenamento de mensagens de somente leitura. Por exemplo, uma empresa de relatórios de crédito poderia usar um repositório de somente leitura para permitir que seus clientes ou funcionários ver, mas não alterar relatórios de crédito individuais. A escolha de fazer com que uma mensagem de somente leitura armazenar tem implicações para a estrutura do provedor de armazenamento de e para o store em si. Por exemplo, um armazenamento de mensagens somente leitura não pode ter uma pasta de caixa de saída, porque e clientes MAPI seriam solicitar a criação de novas mensagens de saída nessa pasta. Da mesma forma, é responsabilidade do provedor de repositório para garantir a integridade do mecanismo de armazenamento subjacente.
  
Há três sinalizadores que podem ser definidos na propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do armazenamento de mensagens que oferecem suporte a diferentes níveis de acesso somente leitura. O sinalizador STORE_READONLY indica que todas as [IMAPIProp: IUnknown](imapipropiunknown.md) interfaces de objetos no repositório de mensagem são somente leitura. O sinalizador STORE_MODIFY_OK indica que as mensagens existentes no armazenamento de mensagens podem ser modificadas, mas novas pastas e mensagens não podem ser criadas. O sinalizador STORE_CREATE_OK indica que as novas mensagens e pastas podem ser criadas, mas indica que nada sobre se a objetos existentes podem ser modificados. 
  
O fato de que os clientes MAPI e o MAPI spooler talvez não sejam capazes de criar, modificar ou excluir objetos no repositório de mensagem não significa que nunca altere o conteúdo do mecanismo de armazenamento subjacente. Nem significa que seu provedor de armazenamento nunca precisa de permissão de gravação para o mecanismo de armazenamento subjacente. Em algumas circunstâncias essas duas condições podem aplicar, mas não no caso geral de uma mensagem de somente leitura armazenar. O nível de acesso que o seu provedor de armazenamento requer e ou não o seu provedor de armazenamento nunca muda dados em que o mecanismo de armazenamento subjacente principalmente depende da natureza específica do provedor de armazenamento.
  
Por exemplo, se você estiver escrevendo um provedor de armazenamento para fornecer a clientes MAPI acesso a um banco de dados armazenado em um dispositivo de CD-ROM, o mecanismo de armazenamento subjacente não é possível alterar e seu provedor de armazenamento pode ter permissão somente leitura para ele. Se, no entanto, você está escrevendo um provedor de armazenamento para fornecer a clientes MAPI acesso somente leitura para um banco de dados de pasta pública, mas o provedor de repositório precisa acompanhar o status de lido/de mensagens para cada usuário, o provedor de armazenamento precisará gravar novos dados para o mecanismo de armazenamento subjacente. Entretanto, nem exemplo o provedor de armazenamento nunca tem que criar, modificar ou excluir pastas ou mensagens por solicitação dos clientes MAPI ou o spooler MAPI.
  
A lista de short dos motivos que um provedor de armazenamento precisaria gravar dados em um mecanismo de armazenamento subjacente que seja somente leitura é da seguinte maneira:
  
- Para armazenar o lido/status de mensagens.
    
- Para implementar notificações de leitura/nonread. 
    
- Para armazenar os modos de exibição.
    
- Para armazenar em cache os índices persistentes para ordens de classificação de pasta definida pelo usuário.
    
- Para armazenar a ordem de classificação do conteúdo de uma pasta (suporte [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)).
    
- Para armazenar os critérios de pesquisa, pesquisa de estado e resultados, se o provedor de armazenamento de mensagem suporta pesquisas (suporte [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)).
    
Se o seu provedor de armazenamento de mensagem nunca pode gravar dados para o mecanismo de armazenamento subjacente, precisará implementar esses recursos usando um mecanismo de armazenamento distinto fora o mecanismo de armazenamento subjacente. Por exemplo, um provedor de armazenamento de mensagem de somente leitura poderia armazenar o lido/status de mensagens no repositório em um arquivo no computador do usuário. Essa estratégia apresenta as dificuldades adicionais, mas pode ser a maneira feasable somente para somente leitura mensagem provedores de armazenamento para implementar alguns recursos. Por exemplo, manter o conteúdo do mecanismo de armazenamento distinto sincronizado com os objetos no armazenamento de mensagens é mais difícil que armazenar o status de lido/diretamente no repositório de mensagem em si.
  
Pesquisando apresenta uma complicação adicional para provedores de armazenamento de mensagem de somente leitura. Clientes usam a pasta especificada na propriedade de **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) do objeto repositório de mensagem para localizar a pasta usada para resultados de pesquisa. Provedores de armazenamento de mensagem de somente leitura geralmente não é possível instalar uma pasta de resultados de pesquisa permanente para o repositório de mensagem. Nessa situação, o provedor de armazenamento de mensagem deve armazenar um identificador de entrada na propriedade **PR_FINDER_ENTRYID** que possa reconhecer quando os clientes abrem pastas para que ele possa criar dinamicamente uma pasta de resultados de pesquisa em vez de leitura de um partir do mecanismo de armazenamento subjacente. No entanto, como vários provedores de armazenamento de mensagem de somente leitura criar todas as suas pastas dinamicamente, isso normalmente não é uma quantidade excessiva de uma carga. 
  
O fato de que o seu provedor de armazenamento de mensagens é somente leitura é anunciado na propriedade **PR_STORE_SUPPORT_MASK** do objeto de provedor de repositório. No entanto, não contam nos clientes respeitar essa propriedade; código do seu provedor de repositório imponha o status somente leitura do mecanismo de armazenamento subjacente. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor do repositório de mensagens MAPI](developing-a-mapi-message-store-provider.md)

