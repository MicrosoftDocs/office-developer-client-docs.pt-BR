---
title: Repositórios de mensagens somente leitura
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
# <a name="read-only-message-stores"></a>Repositórios de mensagens somente leitura

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um repositório de mensagens somente leitura é aquele no qual nem o cliente MAPI nem o spooler MAPI podem criar, modificar ou excluir os objetos no repositório de mensagens. Há muitas razões pelas quais você pode querer implementar um repositório de mensagens somente leitura. Por exemplo, uma empresa de relatórios de crédito pode usar um repositório somente leitura para permitir que seus clientes ou funcionários vejam, mas não alterem relatórios de crédito individuais. Optar por fazer com que um repositório de mensagens somente leitura tenha implicações para a estrutura do provedor da loja e para a própria loja. Por exemplo, um repositório de mensagens somente leitura não pode ter uma pasta de saída, porque os clientes MAPI solicitariam que novas mensagens de saída sejam criadas nessa pasta. Da mesma forma, é responsabilidade do provedor da loja garantir a integridade do mecanismo de armazenamento subjacente.
  
Há três sinalizadores que podem ser definidos na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do repositório de mensagens que oferecem suporte a diferentes níveis de acesso somente leitura. O sinalizador STORE_READONLY indica que todas as interfaces [IMAPIProp: IUnknown](imapipropiunknown.md) nos objetos no repositório de mensagens são somente leitura. O sinalizador STORE_MODIFY_OK indica que as mensagens existentes no repositório de mensagens podem ser modificadas, mas não é possível criar novas pastas e mensagens. O sinalizador STORE_CREATE_OK indica que novas mensagens e pastas podem ser criadas, mas indica Nothing se os objetos existentes podem ser modificados. 
  
O fato de que os clientes MAPI e o spooler MAPI podem não conseguir criar, modificar ou excluir objetos no repositório de mensagens não significa que o conteúdo do mecanismo de armazenamento subjacente nunca mudará. O não significa que seu provedor de repositório nunca precisa de permissão de gravação para o mecanismo de armazenamento subjacente. Em algumas circunstâncias, essas duas condições podem ser aplicadas, mas não no caso geral de um repositório de mensagens somente leitura. O nível de acesso exigido pelo provedor da loja e se o provedor de repositórios ou não altera os dados no mecanismo de armazenamento subjacente depende principalmente da natureza específica do provedor de armazenamento.
  
Por exemplo, se você estiver escrevendo um provedor de repositório para conceder acesso de clientes MAPI a um banco de dados armazenado em um dispositivo de CD-ROM, o mecanismo de armazenamento subjacente não poderá mudar e seu provedor de repositório poderá ter permissão somente leitura para ele. Se, no entanto, você estiver gravando um provedor de repositório para conceder acesso somente leitura para clientes MAPI a um banco de dados de pasta pública, mas o provedor de armazenamento precisar controlar o status de leitura/não leitura de mensagens para cada usuário, o provedor de armazenamento precisará gravar novos dados no mecanismo de armazenamento subjacente. No enTanto, em nenhum exemplo, o provedor de repositório já precisa criar, modificar ou excluir pastas ou mensagens na solicitação de clientes MAPI ou no spooler MAPI.
  
A pequena lista de motivos pelos quais um provedor de armazenamento precisaria gravar dados em um mecanismo de armazenamento subjacente que, de outra forma, é somente leitura é o seguinte:
  
- Para armazenar o status de leitura/não leitura de mensagens.
    
- Para implementar notificações de leitura/não leitura. 
    
- Para armazenar modos de exibição.
    
- Para armazenar em cache índices persistentes para ordens de classificação de pastas definidas pelo usuário.
    
- Para armazenar a ordem de classificação do conteúdo de uma pasta (suportando [IMAPIFolder:: SaveContentsSort](imapifolder-savecontentssort.md)).
    
- Para armazenar critérios de pesquisa, estado de pesquisa e resultados, se o provedor de repositório de mensagens oferecer suporte a pesquisas (suportando [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md)).
    
Se o seu provedor de repositório de mensagens nunca puder gravar dados no mecanismo de armazenamento subjacente, será necessário implementar esses recursos usando um mecanismo de armazenamento separado fora do mecanismo de armazenamento subjacente. Por exemplo, um provedor de repositório de mensagens somente leitura pode armazenar o status de leitura/não leitura de mensagens no repositório em um arquivo no computador do usuário. Essa estratégia apresenta dificuldades adicionais, mas pode ser a única maneira feasable de provedores de repositórios de mensagens somente leitura para implementar alguns recursos. Por exemplo, manter o conteúdo do mecanismo de armazenamento separado sincronizado com os objetos no repositório de mensagens é mais difícil do que armazenar o status de leitura/não leitura diretamente no próprio repositório de mensagens.
  
A pesquisa apresenta uma complicação adicional para provedores de repositório de mensagens somente leitura. Os clientes usam a pasta especificada na propriedade **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) do objeto Message Store para localizar a pasta usada para resultados da pesquisa. Provedores de repositório de mensagens somente leitura geralmente não podem instalar uma pasta de resultados de pesquisa permanente no repositório de mensagens. Nessa situação, o provedor do repositório de mensagens deve armazenar um identificador de entrada na propriedade **PR_FINDER_ENTRYID** que ele pode reconhecer quando os clientes abrem pastas para que possa criar dinamicamente uma pasta de resultados de pesquisa em vez de ler uma da mecanismo de armazenamento subjacente. No enTanto, como muitos provedores de repositório de mensagens somente leitura criam todas as pastas de forma dinâmica, isso geralmente não é muito difícil. 
  
O fato de que seu provedor de repositório de mensagens é somente leitura é anunciado na propriedade **PR_STORE_SUPPORT_MASK** do objeto Provider Store. No enTanto, não conte com os clientes para respeitar essa propriedade; o código do provedor da loja deve impor o status somente leitura do mecanismo de armazenamento subjacente. 
  
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

