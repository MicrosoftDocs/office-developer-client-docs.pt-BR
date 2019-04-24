---
title: Resolver o nome de um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328669"
---
# <a name="resolving-a-recipient-name"></a>Resolver o nome de um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando uma mensagem é endereçada, uma lista de destinatários é criada com propriedades relacionadas a cada destinatário. No momento em que a mensagem é enviada, uma dessas propriedades deve ser o identificador de entrada de longo prazo do destinatário. Para garantir que cada destinatário inclua a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), passe a estrutura [das ADRLIST](adrlist.md) descrevendo sua lista de destinatários no conteúdo do parâmetro _lpAdrList_ em uma chamada para [IAddrBook:: ResolveName](iaddrbook-resolvename.md).
  
 **** O resolvedor começa o processamento, ignorando as entradas na estrutura **das ADRLIST** que já foram resolvidas, conforme indicado pela presença de um identificador de entrada no **SPropValue** da estrutura [ADRENTRY](adrentry.md) correspondente Storage. Em seguida **** , ResolveName atribui automaticamente identificadores de entrada únicos a dois tipos de destinatários: 
  
- Destinatários com um endereço formatado como um endereço da Internet
    
- Destinatários com um endereço formatado da seguinte maneira:
    
     `displayname[address type:email address]`
    
Para todas as entradas restantes **** , ResolveName procura no catálogo de endereços uma correspondência exata no nome de exibição. **** O resolvedor usa a propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar o conjunto de contêineres a ser pesquisado e a ordem de pesquisa. MAPI chama o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de todos os contêineres para tentar resolver todos os nomes. Como alguns contêineres não oferecem **** suporte a ResolveNames, se o contêiner retornar MAPI_E_NO_SUPPORT, MAPI aplica uma restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) em relação a sua tabela de conteúdo. Todos os contêineres do catálogo de endereços são necessários para dar suporte à resolução de nomes com essa restrição. Depois que todos os nomes forem resolvidos, não serão feitas outras chamadas de contêiner. Se todos os contêineres tiverem sido chamados, mas os nomes ambíguos ou não resolvidos permanecerem, MAPI exibirá uma caixa de diálogo, se possível, para solicitar que o usuário resolva os nomes restantes.
  
A restrição **PR_ANR** corresponde ao valor da propriedade **PR_ANR** em relação ao nome de exibição na estrutura **das ADRLIST** . Limitar o modo de exibição da tabela de conteúdo de um contêiner com a restrição de propriedade **PR_ANR** faz com que o provedor de catálogo de endereços execute um tipo de pesquisa de melhor adivinhação, correspondendo à propriedade que faz sentido para o provedor. Por exemplo, um provedor de catálogo de endereços sempre pode coincidir nomes na lista de destinatários em relação ao **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), enquanto outro pode permitir que um administrador selecione a propriedade.
  
 **Para definir uma restrição de propriedade PR_ANR em uma tabela de conteúdo do contêiner de catálogo de endereços**
  
1. Crie uma estrutura [SRestriction](srestriction.md) conforme mostrado no código a seguir: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Chame o método imApitable [:: Restrict](imapitable-restrict.md) da tabela de conteúdo, passando a estrutura **SRestriction** como o parâmetro _lpRestriction_ . 
    

