---
title: Implementando a resolução de nomes
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
# <a name="implementing-name-resolution"></a>Implementando a resolução de nomes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de agendamento são responsáveis por oferecer suporte à resolução de nomes — o processo de associação de um identificador de entrada a um nome de exibição. Os clientes iniciam a resolução de nomes quando chamam [IAddrBook::ResolveName](iaddrbook-resolvename.md) para garantir que cada membro da lista de destinatários de uma mensagem de saída corresponda a um endereço válido. 
  
Seu provedor pode dar suporte à resolução de nomes:
  
- Suporte à **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)), um requisito para todos os contêineres de agenda de endereços.
    
- Implementar o método [IABContainer::ResolveNames,](iabcontainer-resolvenames.md) uma opção para todos os contêineres de agendamento de endereços. 
    
Se você optar por dar suporte a **IABContainer::ResolveNames**, tente localizar uma combinação exata para cada nome de exibição não resolvido na estrutura [ADRLIST](adrlist.md) passada com o parâmetro _lpAdrList._ Você pode identificar um nome de exibição não resolvido porque está faltando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) na matriz de valores de propriedade em seu **membro aEntries** da estrutura **ADRLIST.** Ignore todas as entradas que tenham zero propriedades associadas a elas. 
  
Relatar o resultado de sua tentativa de resolução no parâmetro  _lpFlagList,_ uma matriz de sinalizadores que corresponde à matriz de nomes para exibição  _em lpAdrList_. Os sinalizadores são posicionais de forma que o primeiro sinalizador corresponda ao primeiro membro **aEntries** na estrutura **ADRLIST,** o segundo sinalizador corresponde ao segundo membro **aEntries** e assim por diante. 
  
Há três resultados possíveis para cada entrada não resolvida:
  
- Nenhuma combinação foi encontrada, o que significa que nenhuma das entradas em suas entradas de contêiner corresponder à entrada na estrutura **ADRLIST.** Defina a entrada correspondente no  _parâmetro lpFlagList_ como MAPI_UNRESOLVED. 
    
- Várias combinações podem ser encontradas, o que significa que há várias entradas de contêiner que coincidem com a entrada na **estrutura ADRLIST.** Defina a entrada correspondente no  _parâmetro lpFlagList_ como MAPI_AMBIGUOUS. Não altere o número de entradas na estrutura **ADRLIST.** 
    
- Uma combinação exata pode ser encontrada, o que significa que há apenas uma entrada de contêiner que corresponde à entrada na **estrutura ADRLIST.** Defina o membro correspondente no _parâmetro lpFlagList_ como MAPI_RESOLVED e adicione o identificador de entrada à matriz de propriedades associadas à **entrada ADRLIST.** 
    
Se você optar por não dar suporte a **IABContainer::ResolveNames,** retorne MAPI_E_NO_SUPPORT de sua implementação.
  
Todos os provedores de livro de endereços são necessários para dar suporte **à** resolução de nomes ambíguos — PR_ANR restrição de propriedade — nos índices de conteúdo de seus contêineres. Para fornecer esse suporte, manipular a restrição de PR_ANR em sua implementação de [IMAPITable::Restrict](imapitable-restrict.md) executando um tipo de pesquisa de "melhor suposição", correspondendo a uma ou mais propriedades específicas que fazem sentido para seu provedor. Você pode optar por usar a mesma propriedade ou propriedades sempre, como **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) ou permitir que um administrador escolha em uma lista de propriedades aceitáveis. 
  
Embora a maioria dos provedores fornece sua própria implementação de tabela de conteúdo, você pode personalizar a implementação fornecida por MAPI por meio da [função CreateTable.](createtable.md) No entanto, como a implementação de MAPI não dá suporte a restrições de qualquer tipo, você deve criar um objeto wrapper para incluir uma versão personalizada de **Restrict** que intercepta a chamada. 
  

