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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339736"
---
# <a name="searching-the-address-book"></a>Pesquisar o catálogo de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI permite que os provedores de catálogo de endereços implementem dois níveis de funcionalidade de pesquisa:
  
- Um nível básico que corresponde a um nome especificado com a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) das entradas do catálogo de endereços. Esse nível permite que os usuários, por exemplo, exibam listas de distribuição com nomes que começam com o noroeste ou localizem usuários de mensagens individuais cujo sobrenome seja Brown.
    
- Um nível avançado que corresponde a propriedades diferentes de **PR_DISPLAY_NAME**. Esse nível permite que os usuários, por exemplo, restrinjam ainda mais suas pesquisas e encontrem usuários de mensagens denominados Brown com um tipo de endereço específico.
    
Como os provedores de catálogos de endereços podem oferecer suporte à pesquisa de cada um de seus recipientes no nível básico, em ambos os níveis ou optar por não oferecer suporte a ele, não espere que a pesquisa seja implementada como um recurso padrão. Para determinar se um contêiner específico oferece suporte a pesquisas, tente estabelecer critérios de pesquisa em uma chamada para o método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) . Se **SetSearchCriteria** retornar MAPI_E_NO_SUPPORT, o contêiner não oferece suporte a pesquisas. 
  
Em um contêiner que oferece suporte a pesquisas, recupere critérios estabelecidos chamando [IMAPIContainer:: GetSearchCriteria](imapicontainer-getsearchcriteria.md). Você também pode solicitar que o usuário seja solicitado a fornecer critérios de pesquisa antes de a tabela de conteúdo de um contêiner ser exibida. Para escolher essa opção, defina o sinalizador AB_FIND_ON_OPEN da propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) do contêiner. Depois que o usuário insere os critérios, ele é armazenado como uma restrição e passado para o método **SetSearchCriteria** . A configuração de AB_FIND_ON_OPEN é particularmente útil se você estiver usando um serviço online ou qualquer provedor de catálogo de endereços que tenha um vínculo lento com seus dados. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>Para executar uma pesquisa básica em um contêiner de catálogo de endereços
  
1. Chame o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable do contêiner para abrir sua tabela de conteúdo. 
    
2. Escolha uma técnica de pesquisa que atenda às suas necessidades. As opções incluem:
    
   - [IMAPITable:: FindRow](imapitable-findrow.md) para localizar uma linha específica na tabela. 
    
   - [IMAPITable:: SortTable](imapitable-sorttable.md) para ordenar as linhas na tabela. 
    
   - [IMAPITable:: Restrict](imapitable-restrict.md) para limitar o modo de exibição de tabela. 
    
   - Restrição de propriedade usando a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para resolver nomes ambíguos. Call **IMAPITable:: Restrict** para impor essa restrição. 
    
   - [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) para resolver nomes ambíguos. 
    
3. Call [IMAPITable:: QueryRows](imapitable-queryrows.md) recuperar quaisquer linhas que atendam aos critérios de pesquisa aplicados. **QueryRows** pode retornar zero ou mais linhas correspondentes. 
    
Os métodos **FindRow**, **sortTable**e restrict são métodos Table que estão disponíveis para qualquer tabela que possa ser criada por um cliente ou um provedor de serviços. **** A **propriedade\_PR ANR** Restriction e o método **IABContainer:: ResolveNames** são específicos para provedores de catálogos de endereços e são usados para resolver nomes ambíguos. Nomes ambíguos são entradas em uma lista de destinatários que não têm uma propriedade **PR_ENTRYID** associada a eles. 
  
A **restrição\_ANR de PR** invoca um algoritmo que separa uma cadeia de caracteres em palavras e que corresponde a essas palavras com informações no catálogo de endereços usando correspondência de prefixo. As informações usadas para a correspondência dependem do provedor de catálogo de endereços. Todos os provedores de catálogos de endereços são necessários para dar suporte à restrição **PR_ANR** para seus contêineres de catálogo de endereços. Para obter mais informações, consulte [implementaNdo resolução de nomes](implementing-name-resolution.md).
  
**IABContainer:: ResolveNames** realiza o processamento de restrição **PR_ANR** em vários nomes sem exigir que a tabela de conteúdo do contêiner esteja aberta. Chamar **ResolveNames** uma vez para resolver vários nomes pode ser muito mais rápido do que invocar uma restrição **ANR de PR\_** várias vezes. No enTanto, os provedores de catálogo de endereços **** não são necessários para dar suporte a ResolveNames.
  

