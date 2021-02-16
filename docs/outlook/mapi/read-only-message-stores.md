---
title: Read-Only de Mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 752ff2d6-ca64-4507-adf1-4c054c321203
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 957a7f92963b97e5421bc801a3b046f098d6a08e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405335"
---
# <a name="read-only-message-stores"></a>Read-Only de Mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um armazenamento de mensagens somente leitura é aquele no qual nem o cliente MAPI nem o spooler MAPI podem criar, modificar ou excluir os objetos no armazenamento de mensagens. Há muitos motivos pelos quais você pode querer implementar um armazenamento de mensagens somente leitura. Por exemplo, uma empresa de relatórios de crédito pode usar um armazenamento somente leitura para permitir que seus clientes ou funcionários vejam, mas não alterem relatórios de crédito individuais. Optar por tornar um armazenamento de mensagens somente leitura tem implicações para a estrutura do provedor de armazenamento e para o próprio armazenamento. Por exemplo, um armazenamento de mensagens somente leitura não pode ter uma pasta caixa de saída, porque os clientes MAPI solicitariam que novas mensagens de saída sejam criadas nessa pasta. Da mesma forma, é responsabilidade do provedor da loja garantir a integridade do mecanismo de armazenamento subjacente.
  
Há três sinalizadores que podem ser definidos na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do repositório de mensagens que suportam diferentes níveis de acesso somente leitura. O STORE_READONLY sinalizador indica que todas as interfaces [IMAPIProp : IUnknown](imapipropiunknown.md) em objetos no armazenamento de mensagens são somente leitura. O STORE_MODIFY_OK sinalizador indica que as mensagens existentes no armazenamento de mensagens podem ser modificadas, mas novas pastas e mensagens podem não ser criadas. O STORE_CREATE_OK sinalizador indica que novas mensagens e pastas podem ser criadas, mas não indica se objetos existentes podem ser modificados. 
  
O fato de que os clientes MAPI e o spooler MAPI podem não ser capazes de criar, modificar ou excluir objetos no armazenamento de mensagens não significa que o conteúdo do mecanismo de armazenamento subjacente nunca mude. Nem significa que seu provedor de armazenamento nunca precisa de permissão de gravação para o mecanismo de armazenamento subjacente. Em algumas circunstâncias, essas duas condições podem se aplicar, mas não no caso geral de um armazenamento de mensagens somente leitura. O nível de acesso que seu provedor de armazenamento requer e se o provedor de armazenamento nunca altera os dados no mecanismo de armazenamento subjacente depende principalmente da natureza específica do seu provedor de armazenamento.
  
Por exemplo, se você estiver escrevendo um provedor de armazenamento para dar aos clientes MAPI acesso a um banco de dados armazenado em um dispositivo cd-ROM, o mecanismo de armazenamento subjacente não pode mudar e seu provedor de armazenamento pode ter permissão de somente leitura para ele. No entanto, se você estiver escrevendo um provedor de armazenamento para dar aos clientes MAPI acesso somente leitura a um banco de dados de pasta pública, mas o provedor de armazenamento precisar acompanhar o status de leitura/não lida de mensagens para cada usuário, o provedor de armazenamento precisará gravar novos dados no mecanismo de armazenamento subjacente. No entanto, em nenhum dos exemplos o provedor de armazenamento precisa criar, modificar ou excluir pastas ou mensagens a pedido de clientes MAPI ou do spooler MAPI.
  
A pequena lista de motivos pelos quais um provedor de armazenamento precisaria gravar dados em um mecanismo de armazenamento subjacente que, de outra forma, é somente leitura é a seguinte:
  
- Para armazenar o status de leitura/não lida das mensagens.
    
- Para implementar notificações de leitura/não lidas. 
    
- Para armazenar exibições.
    
- Para armazenar em cache índices persistentes para ordens de classificação de pasta definidas pelo usuário.
    
- Para armazenar a ordem de classificação do conteúdo de uma pasta (dando suporte a [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)).
    
- Para armazenar critérios de pesquisa, estado de pesquisa e resultados, se o provedor de armazenamento de mensagens oferecer suporte a pesquisas (dando suporte a [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)).
    
Se seu provedor de armazenamento de mensagens nunca puder gravar dados no mecanismo de armazenamento subjacente, ele precisará implementar esses recursos usando um mecanismo de armazenamento separado fora do mecanismo de armazenamento subjacente. Por exemplo, um provedor de armazenamento de mensagens somente leitura pode armazenar o status de leitura/não lida das mensagens no armazenamento em um arquivo no computador do usuário. Essa estratégia apresenta dificuldades adicionais, mas pode ser a única maneira para provedores de armazenamento de mensagens somente leitura implementarem alguns recursos. Por exemplo, manter o conteúdo do mecanismo de armazenamento separado sincronizado com os objetos no armazenamento de mensagens é mais difícil do que armazenar o status de leitura/não lido diretamente no próprio armazenamento de mensagens.
  
Pesquisar apresenta uma complicação adicional para provedores de armazenamento de mensagens somente leitura. Os clientes usam a pasta especificada na propriedade PR_FINDER_ENTRYID ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) do objeto de armazenamento de mensagens para localizar **a** pasta usada para resultados de pesquisa. Os provedores de armazenamento de mensagens somente leitura geralmente não podem instalar uma pasta de resultados de pesquisa permanente no armazenamento de mensagens. Nessa situação, o provedor de armazenamento de mensagens deve armazenar um identificador de entrada na propriedade PR_FINDER_ENTRYID que possa reconhecer quando os clientes abrirem pastas para que ele possa criar dinamicamente uma pasta de resultados de pesquisa em vez de ler uma **do** mecanismo de armazenamento subjacente. No entanto, como muitos provedores de armazenamento de mensagens somente leitura criam todas as pastas dinamicamente, isso geralmente não é uma carga muito grande. 
  
O fato de seu provedor de armazenamento de mensagens ser somente leitura é anunciado na propriedade de PR_STORE_SUPPORT_MASK do provedor **de** armazenamento. No entanto, não conte com clientes para respeitar essa propriedade; o código do provedor de armazenamento deve impor o status somente leitura do mecanismo de armazenamento subjacente. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

