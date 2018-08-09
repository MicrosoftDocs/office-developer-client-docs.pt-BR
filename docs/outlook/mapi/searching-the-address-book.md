---
title: Pesquisar o catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20ff2b63-e4a3-4ba9-bad0-2c1873fb69b5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6673e1d51a7c030a35a7c5c3cbc955341afba299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770348"
---
# <a name="searching-the-address-book"></a>Pesquisar o catálogo de endereços

**Aplica-se a**: Outlook 
  
MAPI permite que os provedores de catálogo de endereços implementar dois níveis de funcionalidade de pesquisa:
  
- Um nível básico que corresponda a um nome especificado com a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) das entradas do catálogo de endereços. Este nível permite que os usuários, por exemplo, para exibir listas de distribuição com nomes começando com Noroeste ou localizar usuários individuais de mensagens cujo sobrenome seja marrom.
    
- Um nível avançado que corresponda a propriedades que não seja **PR_DISPLAY_NAME**. Este nível permite que os usuários, por exemplo, para reduzir ainda mais suas pesquisas e localizar mensagens chamados Brown com um tipo de endereço específico de usuários.
    
Porque oferece suporte a procurando por cada um dos seus contêineres no nível básico, em ambos os níveis, ou optar por não suportá-las em todos os provedores de catálogo de endereços, não espera pesquisando para ser implementado como um recurso padrão. Para determinar se um determinado recipiente suporta pesquisas, tente estabelecer critérios de pesquisa em uma chamada para seu método de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) . Se **definir SetSearchCriteria** retornar MAPI_E_NO_SUPPORT, o contêiner não oferece suporte a pesquisas. 
  
Em um contêiner que suporta pesquisas, recupere critérios estabelecidos chamando [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md). Você também pode solicitar que o usuário solicitado para os critérios de pesquisa antes de tabela de conteúdo de um contêiner é exibida. Para escolher essa opção, defina o sinalizador AB_FIND_ON_OPEN da propriedade de **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) do contêiner. Depois que o usuário insere os critérios, é armazenada como uma restrição e passada para o método **definir SetSearchCriteria** . Definindo AB_FIND_ON_OPEN é particularmente útil se você estiver usando um serviço online ou qualquer provedor de catálogo de endereços que tem um vínculo lento para seus dados. 
  
### <a name="to-perform-a-basic-search-in-an-address-book-container"></a>Para executar uma pesquisa básica em um contêiner de catálogo de endereços
  
1. Chame o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) do contêiner para abrir a tabela de seu conteúdo. 
    
2. Escolha uma técnica de pesquisa que atenda às suas necessidades. As opções incluem:
    
   - [IMAPITable:: FindRow](imapitable-findrow.md) para localizar uma linha específica na tabela. 
    
   - [IMAPITable:: SortTable](imapitable-sorttable.md) às linhas de pedido na tabela. 
    
   - [IMAPITable:: Restrict](imapitable-restrict.md) para limitar o modo de exibição de tabela. 
    
   - Restrição de propriedade usando a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para resolver nomes ambíguos. Chame **IMAPITable:: Restrict** para impor essa restrição. 
    
   - [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) para resolver nomes de ambíguos. 
    
3. Chame [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas que atendem aos critérios de pesquisa aplicados. **QueryRows** pode retornar zero ou mais linhas correspondentes. 
    
Os métodos **FindRow**, **SortTable**e **Restrict** são tabela que estão disponíveis para qualquer tabela que pode ser criada por um cliente ou um provedor de serviços. O **PR\_ANR** método **IABContainer:: ResolveNames** e restrição de propriedade são específicos para provedores de catálogo de endereços e são usados para resolver nomes ambíguos. Nomes ambíguos são entradas em uma lista de destinatários que não possuem uma propriedade **PR_ENTRYID** associada a eles. 
  
O **PR\_ANR** restrição invoca um algoritmo que separa uma cadeia de caracteres em palavras e faz a correspondência dessas palavras com informações no catálogo de endereços usando a correspondência de prefixo. As informações utilizadas para a correspondência dependem do provedor de catálogo de endereços. Todos os provedores de catálogo de endereços são necessárias para dar suporte a restrição de **PR_ANR** para seus contêineres do catálogo de endereços. Para obter mais informações, consulte [Implementando a resolução de nome](implementing-name-resolution.md).
  
**IABContainer:: ResolveNames** realiza a restrição de **PR_ANR** de processamento em vários nomes sem a necessidade de tabela de conteúdo do contêiner para ser aberto. Chamar **ResolveNames** uma vez para resolver nomes de vários pode ser muito mais rápido do que chamar uma **PR\_ANR** restrição várias vezes. No entanto, provedores de catálogo de endereços não são necessárias para dar suporte a **ResolveNames**.
  

