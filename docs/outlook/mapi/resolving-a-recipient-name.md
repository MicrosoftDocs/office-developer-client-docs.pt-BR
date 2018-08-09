---
title: Resolver o nome de um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770253"
---
# <a name="resolving-a-recipient-name"></a>Resolver o nome de um destinatário

  
  
**Aplica-se a**: Outlook 
  
Quando uma mensagem é encaminhada, uma lista de destinatários é criada com propriedades relacionadas a cada destinatário. No momento em que a mensagem é enviada, uma dessas propriedades deve ser um identificador de entrada a longo prazo do destinatário. Para garantir que cada destinatário inclui a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), passe a estrutura [ADRLIST](adrlist.md) descrevendo sua lista de destinatários no conteúdo do parâmetro _lpAdrList_ em uma chamada para [IAddrBook:: ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** inicialmente processamento, ignorando as entradas na estrutura de **ADRLIST** que já foram resolvidas, conforme indicado pela presença de um identificador de entrada no correspondente da estrutura [ADRENTRY](adrentry.md) **SPropValue** matriz. Em seguida, **ResolveName** atribuirá automaticamente identificadores de entrada únicos a dois tipos de destinatários: 
  
- Destinatários com um endereço formatado como um endereço de Internet
    
- Destinatários com um endereço formatado como se segue:
    
     `displayname[address type:email address]`
    
Para todas as entradas restantes, **ResolveName** procura o catálogo de endereços uma correspondência exata no nome para exibição. **ResolveName** usa a propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar o conjunto de contêineres a pesquisa e a ordem de pesquisa. O método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de cada contêiner para tentar resolver todos os nomes de chamadas de MAPI. Porque alguns contêineres não suportam **ResolveNames**, se o contêiner retornará MAPI_E_NO_SUPPORT, MAPI aplica uma restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) em relação à tabela seu conteúdo. Todos os contêineres do catálogo de endereços são necessários para dar suporte a resolução de nomes com essa restrição. Depois que todos os nomes forem resolvidos, nenhuma outra são feitas chamadas do contêiner. Se todos os contêineres tiverem sido chamados, mas nomes ambíguos ou não resolvidos permanecerão, MAPI exibe uma caixa de diálogo se possível para solicitar ao usuário para resolver os nomes restantes.
  
A restrição de **PR_ANR** corresponde ao valor da propriedade **PR_ANR** contra o nome para exibição na estrutura **ADRLIST** . Limitando a exibição da tabela de conteúdo de um contêiner com a restrição de propriedade **PR_ANR** faz com que o provedor de catálogo de endereços executar um tipo de "melhor adivinhar" da pesquisa, correspondência contra a propriedade que faz sentido para o provedor. Por exemplo, um provedor de catálogo de endereços sempre pode corresponder nomes na lista de destinatários contra **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) enquanto outra pode permitir que um administrador selecionar a propriedade.
  
 **Para definir uma restrição de propriedade PR_ANR na tabela de conteúdo de um contêiner catálogo de endereços**
  
1. Crie uma estrutura [SRestriction](srestriction.md) , conforme mostrado no seguinte código: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Chame o conteúdo [IMAPITable:: Restrict](imapitable-restrict.md) método da tabela, passando a estrutura **SRestriction** como o parâmetro _lpRestriction_ . 
    

