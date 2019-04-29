---
title: Implementar a pesquisa avançada
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
# <a name="implementing-advanced-searching"></a>Implementar a pesquisa avançada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns contêineres do catálogo de endereços dão suporte a um recurso de pesquisa avançada que permite que os clientes pesquisem propriedades diferentes de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Para oferecer suporte a pesquisas avançadas, seu provedor deve implementar um contêiner especial que possa ser acessado através da propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de seus outros contêineres. **PR_SEARCH** contém um objeto Container que fornece acesso a uma tabela de exibição que descreve a caixa de diálogo usada para inserir e editar os critérios de pesquisa avançados. 
  
 **Para oferecer suporte à pesquisa avançada**
  
1. Defina uma propriedade para cada critério de pesquisa.
    
2. Na seção de código no seu contêiner [IMAPIProp::](imapiprop-openproperty.md) método OpenProperty que manipula a propriedade **PR_SEARCH** : 
    
1. Verifique se o cliente está solicitando a interface **IMAPIContainer** . Se uma interface inadequada estiver sendo solicitada, falhará e retornará MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Criar um novo objeto de pesquisa que ofereça suporte à interface **IMAPIContainer** . 
    
3. Neste ponto, será feita uma chamada para o método **IMAPIProp:: OpenProperty** do seu contêiner de pesquisa para recuperar sua propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). Seu provedor deve fornecer uma tabela de exibição, geralmente por meio de uma chamada a [BuildDisplayTable](builddisplaytable.md), que descreve a caixa de diálogo de pesquisa avançada do contêiner.
    
4. MAPI exibe a caixa de diálogo pesquisa, permitindo que o usuário insira os critérios apropriados. Quando o usuário tiver concluído, o MAPI chamará o método [IMAPIProp::](imapiprop-setprops.md) SetProps do contêiner para armazenar os critérios de pesquisa. 
    
5. Uma chamada será feita para solicitar a tabela de conteúdo do seu contêiner de pesquisa. Preencha a tabela de conteúdo com todas as entradas no contêiner que correspondam aos critérios.
    

