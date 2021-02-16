---
title: Pesquisar o catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d40419291f4b09c5880a769ce231015511e8f269
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424368"
---
# <a name="searching-the-address-book"></a>Pesquisar o catálogo de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI permite que os provedores de agendas implementem dois níveis de funcionalidade de pesquisa:
  
- Um nível básico que corresponde a um nome especificado com a **propriedade PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) das entradas do livro de endereços. Esse nível permite aos usuários, por exemplo, exibir listas de distribuição com nomes que começam com Noroeste ou localizar usuários de mensagens individuais cujo sobrenome é Marrom.
    
- Um nível avançado que corresponde a propriedades diferentes de **PR_DISPLAY_NAME**. Esse nível permite aos usuários, por exemplo, restringir ainda mais suas pesquisas e encontrar usuários de mensagens chamados Marrom com um tipo de endereço específico.
    
Como os provedores de agendas de endereços podem dar suporte à pesquisa de cada um de seus contêineres no nível básico, em ambos os níveis ou optar por não dar suporte a ele, não espere que a pesquisa seja implementada como um recurso padrão. Para determinar se um contêiner específico oferece suporte a pesquisas, tente estabelecer critérios de pesquisa em uma chamada para seu método [IMAPIContainer::SetSearchCriteria.](imapicontainer-setsearchcriteria.md) Se **SetSearchCriteria** retornar MAPI_E_NO_SUPPORT, o contêiner não suportará pesquisas. 
  
Em um contêiner que oferece suporte a pesquisas, recupere critérios estabelecidos chamando [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). Você também pode solicitar que o usuário seja solicitado a solicitar critérios de pesquisa antes que a tabela de conteúdo de um contêiner seja exibida. Para escolher essa opção, defina o AB_FIND_ON_OPEN da propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags)](pidtagcontainerflags-canonical-property.md)do contêiner. Depois que o usuário inscreva os critérios, ele é armazenado como uma restrição e passado para o **método SetSearchCriteria.** Definir AB_FIND_ON_OPEN é particularmente útil se você estiver usando um serviço online ou qualquer provedor de agendas que tenha um link lento para seus dados. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>Para realizar uma pesquisa básica em um contêiner de agendas
  
1. Chame o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) do contêiner para abrir sua tabela de conteúdo. 
    
2. Escolha uma técnica de pesquisa que atenda às suas necessidades. As opções incluem:
    
   - [IMAPITable::FindRow](imapitable-findrow.md) para localizar uma linha específica na tabela. 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md) para ordenar linhas na tabela. 
    
   - [IMAPITable::Restrict](imapitable-restrict.md) para limitar o exibição de tabela. 
    
   - Restrição de propriedade **usando a PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para resolver nomes ambíguos. Chame **IMAPITable::Restrict** para impor essa restrição. 
    
   - [IABContainer::ResolveNames](iabcontainer-resolvenames.md) para resolver nomes ambíguos. 
    
3. Chame [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar todas as linhas que atendem aos critérios de pesquisa aplicados. **QueryRows** pode retornar zero ou mais linhas correspondentes. 
    
Os **métodos FindRow**, **SortTable** e **Restrict** são métodos de tabela que estão disponíveis para qualquer tabela que pode ser criada, por um cliente ou um provedor de serviços. A **\_ restrição** de propriedade PR ANR e o método **IABContainer::ResolveNames** são específicos para provedores de agendamento de endereços e são usados para resolver nomes ambíguos. Nomes ambíguos são entradas em uma lista de destinatários que não têm uma **PR_ENTRYID** propriedade associada a elas. 
  
A **\_ restrição PR ANR** invoca um algoritmo que separa uma cadeia de caracteres em palavras e corresponde a essas palavras com informações no livro de endereços usando correspondência de prefixo. As informações usadas para a correspondência dependem do provedor de agendas. Todos os provedores de agendas de endereços são necessários para dar suporte **PR_ANR** restrição para seus contêineres de livro de endereços. Para obter mais informações, consulte [Implementando a resolução de nomes.](implementing-name-resolution.md)
  
**IABContainer::ResolveNames** executa  PR_ANR de restrição em vários nomes sem exigir que a tabela de conteúdo do contêiner seja aberta. Chamar **ResolveNames uma** vez para resolver vários nomes pode ser muito mais rápido do que invocar uma restrição **\_ ANR de PR** várias vezes. No entanto, os provedores de livro de endereços não são necessários para dar suporte **a ResolveNames**.
  

