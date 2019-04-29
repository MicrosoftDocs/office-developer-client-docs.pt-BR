---
title: Implementar a resolução de nomes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 15c1d502947865c02973f4950b6b6fa8109b8e78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434701"
---
# <a name="implementing-name-resolution"></a>Implementar a resolução de nomes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de catálogos de endereços são responsáveis por suportar a resolução de nomes: o processo de associação de um identificador de entrada com um nome de exibição. Os clientes iniciam a resolução de nome quando chamam [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para garantir que cada membro de uma lista de destinatários da mensagem de saída corresponde a um endereço válido. 
  
O provedor pode dar suporte à resolução de nomes:
  
- Suporte à restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), um requisito para todos os contêineres do catálogo de endereços.
    
- Implementar o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) , uma opção para todos os contêineres do catálogo de endereços. 
    
Se você optar por oferecer suporte a **IABContainer:: ResolveNames**, tentar localizar uma correspondência exata para cada nome de exibição não resolvido na estrutura [das ADRLIST](adrlist.md) passada com o parâmetro _lpAdrList_ . Você pode identificá-lo como um nome de exibição não resolvido porque falta a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) na matriz de valor da propriedade em seu membro **aEntries** da estrutura **das ADRLIST** . Ignorar qualquer entrada que tenha zero propriedades associadas. 
  
Informe o resultado da tentativa de resolução no parâmetro _lpFlagList_ , uma matriz de sinalizadores que corresponde à matriz de nomes para exibição no _lpAdrList_. Os sinalizadores são posicionais de forma que o primeiro sinalizador corresponda ao primeiro membro **aEntries** na estrutura **das ADRLIST** , o segundo sinalizador corresponde ao segundo membro do **aEntries** e assim por diante. 
  
Há três resultados possíveis para cada entrada não resolvida:
  
- Nenhuma correspondência foi encontrada, o que significa que nenhuma das entradas em suas entradas de contêiner corresponde à entrada na estrutura **das ADRLIST** . Defina a entrada correspondente no parâmetro _lpFlagList_ como MAPI_UNRESOLVED. 
    
- Várias correspondências podem ser encontradas, o que significa que há várias entradas de contêiner que correspondem à entrada na estrutura **das ADRLIST** . Defina a entrada correspondente no parâmetro _lpFlagList_ como MAPI_AMBIGUOUS. Não altere o número de entradas na estrutura **das ADRLIST** . 
    
- Uma correspondência exata pode ser encontrada, o que significa que há apenas uma entrada de contêiner que corresponde à entrada na estrutura **das ADRLIST** . Defina o membro correspondente no parâmetro _lpFlagList_ como MAPI_RESOLVED e adicione o identificador de entrada à matriz de propriedades associadas à entrada **das ADRLIST** . 
    
Se você optar por não oferecer suporte a **IABContainer:: ResolveNames**, retornar MAPI_E_NO_SUPPORT da sua implementação.
  
Todos os provedores de catálogo de endereços são necessários para dar suporte à resolução de nomes ambíguos, a restrição de propriedade **PR_ANR** , em suas tabelas de conteúdo de contêineres. Para fornecer esse suporte, manipule a restrição PR_ANR em sua implementação de [IMAPITable:: Restrict](imapitable-restrict.md) executando um tipo de pesquisa "melhor palpite", correspondendo a uma ou mais propriedades específicas que fazem sentido para seu provedor. Você pode optar por usar a mesma propriedade ou propriedades a cada vez, como **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) ou permitir que um administrador escolha em uma lista de propriedades aceitáveis. 
  
Embora a maioria dos provedores forneça sua própria implementação de tabela de conteúdo, você pode personalizar a implementação fornecida [](createtable.md) pelo MAPI através da função CreateTable. No enTanto, como a implementação MAPI não dá suporte a restrições de qualquer tipo, você deve criar um objeto wrapper para incluir uma **** versão personalizada do restrict que intercepta a chamada. 
  

