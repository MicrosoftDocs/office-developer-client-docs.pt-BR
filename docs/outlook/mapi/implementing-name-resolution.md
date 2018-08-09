---
title: Implementar a resolução de nome
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4d55404149baca07a64b75d460bdfb2a8c541725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767428"
---
# <a name="implementing-name-resolution"></a>Implementar a resolução de nome

  
  
**Aplica-se a**: Outlook 
  
Provedores de catálogo de endereços serão responsáveis pelo suporte a resolução de nome — o processo de associar um identificador de entrada com um nome de exibição. Os clientes iniciar a resolução de nomes quando ele liga [IAddrBook::ResolveName](iaddrbook-resolvename.md) para garantir que cada membro da lista de destinatários de uma mensagem de saída corresponde a um endereço válido. 
  
Seu provedor pode oferecer suporte a resolução de nomes por:
  
- Dando suporte a restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), um requisito para todos os contêineres do catálogo de endereços.
    
- Implementando o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) , uma opção para todos os contêineres do catálogo de endereços. 
    
Se você optar por suporte **IABContainer:: ResolveNames**, tenta localizar uma correspondência exata para cada nome de exibição não resolvidos na estrutura [ADRLIST](adrlist.md) passada com o parâmetro _lpAdrList_ . Você pode identifiy um nome para exibição não resolvidos porque a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da matriz de valores de propriedade em seu membro **aEntries** da estrutura **ADRLIST** está faltando. Ignore quaisquer entradas que têm zero propriedades associadas a eles. 
  
Relate o resultado da sua tentativa na resolução no parâmetro _lpFlagList_ , uma matriz dos sinalizadores que corresponde à matriz de nomes de exibição no _lpAdrList_. Os sinalizadores são posicionais, de forma que o primeiro sinalizador corresponde ao primeiro membro **aEntries** na estrutura de **ADRLIST** , o sinalizador segundo corresponde ao membro de **aEntries** segundo e assim por diante. 
  
Há três possíveis resultados para cada entrada não resolvido:
  
- Nenhuma correspondência for encontrada, o que significa que nenhuma das entradas no suas entradas de contêiner corresponder à entrada na estrutura **ADRLIST** . Defina a entrada correspondente no parâmetro _lpFlagList_ para MAPI_UNRESOLVED. 
    
- Várias correspondências podem ser encontradas, o que significa que não existem várias entradas de contêiner que correspondem a entrada na estrutura **ADRLIST** . Defina a entrada correspondente no parâmetro _lpFlagList_ para MAPI_AMBIGUOUS. Não altere o número de entradas na estrutura de **ADRLIST** . 
    
- Uma correspondência exata pode ser encontrada, o que significa que não há entrada de apenas um contêiner que compara a entrada na estrutura **ADRLIST** . Defina o membro correspondente no parâmetro _lpFlagList_ para MAPI_RESOLVED e adicione o identificador de entrada à matriz de propriedades associadas a entrada **ADRLIST** . 
    
Se você escolher não suportar **IABContainer:: ResolveNames**, retorne MAPI_E_NO_SUPPORT da sua implementação.
  
Todos os provedores de catálogo de endereços são necessárias para dar suporte a resolução de nome ambígua — a restrição de propriedade **PR_ANR** — em tabelas de conteúdo dos seus contêineres. Para fornecer esse suporte, lidar com a restrição de PR_ANR na sua implementação de [IMAPITable:: Restrict](imapitable-restrict.md) executando um tipo de "melhor adivinhar" da pesquisa, correspondência com base em uma ou mais propriedades específicas que fazem sentido para seu provedor. Você pode optar por usar a mesma propriedade ou propriedades de cada vez, como **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), ou permitem que um administrador escolher em uma lista das propriedades aceitáveis. 
  
Embora a maioria dos provedores de fornecer sua própria implementação de tabela de conteúdo, você pode personalizar a implementação fornecida pelo MAPI por meio da função [CreateTable](createtable.md) . No entanto, como a implementação de MAPI não oferece suporte a restrições de qualquer tipo, você deve criar um objeto wrapper para incluir uma versão personalizada do **Restrict** que intercepta a chamada. 
  

