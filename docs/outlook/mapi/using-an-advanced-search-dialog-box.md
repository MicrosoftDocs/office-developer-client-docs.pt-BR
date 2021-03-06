---
title: Usando uma caixa de diálogo Pesquisa Avançada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437298"
---
# <a name="using-an-advanced-search-dialog-box"></a>Usando uma caixa de diálogo Pesquisa Avançada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns contêineres de livro de endereços suportam um recurso de pesquisa avançada que permite que os clientes pesquisem em propriedades diferentes de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Contêineres de livro de endereços que suportam pesquisas avançadas têm uma propriedade de objeto de **contêiner chamada PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Esse objeto contêiner fornece acesso a uma tabela de exibição que descreve a caixa de diálogo de pesquisa — uma caixa de diálogo usada para inserir e editar os critérios de pesquisa avançados.
  
 **Para executar uma pesquisa avançada em um contêiner de um livro de endereços**
  
1. Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do  contêiner, especificando PR_SEARCH para a marca de propriedade e IID_IMAPIContainer para o identificador da interface. 
    
2. Chame o método **IMAPIProp::OpenProperty** do objeto de pesquisa, especificando **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) para a marca de propriedade e IID_IMAPITable para o identificador da interface. 
    
3. Chame o método [IMAPIProp::SetProps](imapiprop-setprops.md) do objeto de pesquisa para estabelecer valores para as propriedades a serem usadas na pesquisa avançada. 
    
4. Chame o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) do objeto de pesquisa para salvar os critérios de pesquisa avançados. 
    
Essa sequência de chamadas resulta na disponibilidade de uma restrição quando um cliente chama o método **GetSearchCriteria do** objeto de pesquisa. 
  

