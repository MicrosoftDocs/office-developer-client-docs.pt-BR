---
title: Implementar a pesquisa avançada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4430b52b470b89bd7d81922b98b121b3a455768f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767419"
---
# <a name="implementing-advanced-searching"></a>Implementar a pesquisa avançada

  
  
**Aplica-se a**: Outlook 
  
Alguns recipientes do catálogo de endereços oferecem suporte a um recurso de pesquisando avançado que permite aos clientes pesquisar propriedades que não seja **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Para suportar pesquisas avançadas, seu provedor deve implementar um contêiner especial que pode ser acessado por meio da propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) dos seus outros contêineres. **PR_SEARCH** contém um objeto container que fornece acesso a uma tabela de exibição que descreve a caixa de diálogo usada para inserir e editar os critérios de pesquisa avançada. 
  
 **Para oferecer suporte à pesquisa avançada**
  
1. Defina uma propriedade para cada um dos seus critérios de pesquisa.
    
2. Na seção de código no método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do seu contêiner que manipula a propriedade **PR_SEARCH** : 
    
1. Verifique se o cliente está solicitando a interface **IMAPIContainer** . Se uma interface inadequada é solicitada, falhar e retornar MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Crie um novo objeto de pesquisa que dá suporte à interface **IMAPIContainer** . 
    
3. Neste ponto, vai ser feita uma chamada ao método de **IMAPIProp::OpenProperty** do seu contêiner de pesquisa para recuperar sua propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). Seu provedor deve fornecer uma exibição de tabela, normalmente por meio de uma chamada para [BuildDisplayTable](builddisplaytable.md), que descreve a caixa de diálogo de pesquisa avançada do contêiner.
    
4. MAPI exibe a caixa de diálogo de pesquisa, permitindo que o usuário insira os critérios apropriados. Quando o usuário tiver terminado, MAPI chama o método de [IMAPIProp::SetProps](imapiprop-setprops.md) do contêiner para armazenar os critérios de pesquisa. 
    
5. Será feita uma chamada para solicitar a tabela de conteúdo do seu contêiner de pesquisa. Preenchem a tabela de conteúdo com todas as entradas no contêiner que correspondem aos critérios.
    

