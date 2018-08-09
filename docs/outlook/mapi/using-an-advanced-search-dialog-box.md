---
title: Usar a caixa de diálogo de pesquisa avançada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3c27b859f6d056d3b9a98bd4d71db8e500dff696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770693"
---
# <a name="using-an-advanced-search-dialog-box"></a>Usar a caixa de diálogo de pesquisa avançada

  
  
**Aplica-se a**: Outlook 
  
Alguns recipientes do catálogo de endereços oferecem suporte a um recurso de pesquisando avançado que permite aos clientes pesquisar propriedades que não seja **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Contêineres de catálogo de endereços que oferecem suporte a pesquisas avançadas possuem uma propriedade de objeto de contêiner chamada **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Este objeto de contêiner fornece acesso a uma tabela de exibição que descreve a caixa de diálogo de pesquisa — uma caixa de diálogo usada para inserir e editar os critérios de pesquisa avançada.
  
 **Para realizar uma pesquisa avançada em um contêiner de catálogo de endereços**
  
1. Chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner, especificando **PR_SEARCH** para a marca de propriedade e IID_IMAPIContainer para o identificador de interface. 
    
2. Chame o método de **IMAPIProp::OpenProperty** do objeto de pesquisa, especificando **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) para a marca de propriedade e IID_IMAPITable para o identificador de interface. 
    
3. Chame o método de [IMAPIProp::SetProps](imapiprop-setprops.md) do objeto de pesquisa para estabelecer valores para as propriedades a ser usado na página Pesquisa avançada. 
    
4. Chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do objeto de pesquisa para salvar os critérios de pesquisa avançada. 
    
Esta sequência de chamadas resulta em uma restrição fique disponível quando um cliente chama o método de **obter GetSearchCriteria** do objeto search. 
  

