---
title: Implementando a Pesquisa Avançada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407386"
---
# <a name="implementing-advanced-searching"></a>Implementando a Pesquisa Avançada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns contêineres de livro de endereços suportam um recurso de pesquisa avançada que permite que os clientes pesquisem em propriedades diferentes de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Para dar suporte a pesquisas avançadas, seu provedor deve implementar um contêiner especial que seja acessível por meio da propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de seus outros contêineres. **PR_SEARCH** contém um objeto container que fornece acesso a uma tabela de exibição que descreve a caixa de diálogo usada para inserir e editar os critérios de pesquisa avançados. 
  
 **Para dar suporte à pesquisa avançada**
  
1. Defina uma propriedade para cada um dos seus critérios de pesquisa.
    
2. Na seção do código no método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner que lida com PR_SEARCH **propriedade:** 
    
1. Verifique se o cliente está solicitando a interface **IMAPIContainer.** Se uma interface inadequada estiver sendo solicitada, falhará e retornará MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Crie um novo objeto de pesquisa que suporte a interface **IMAPIContainer.** 
    
3. Neste ponto, será feita uma chamada ao método **IMAPIProp::OpenProperty** do contêiner de pesquisa para recuperar sua **propriedade PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). Seu provedor deve fornecer uma tabela de exibição, normalmente por meio de uma chamada para [BuildDisplayTable](builddisplaytable.md), que descreve a caixa de diálogo de pesquisa avançada do contêiner.
    
4. O MAPI exibe a caixa de diálogo de pesquisa, permitindo que o usuário insira os critérios apropriados. Quando o usuário tiver terminado, o MAPI chamará o método [IMAPIProp::SetProps](imapiprop-setprops.md) do contêiner para armazenar os critérios de pesquisa. 
    
5. Uma chamada será feita para solicitar a tabela de conteúdo do contêiner de pesquisa. Preencha a tabela de conteúdo com todas as entradas no contêiner que corresponderem aos critérios.
    

