---
title: Resolvendo um nome de destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405861"
---
# <a name="resolving-a-recipient-name"></a>Resolvendo um nome de destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando uma mensagem é endereçada, uma lista de destinatários é criada com propriedades relacionadas a cada destinatário. No momento em que a mensagem é enviada, uma dessas propriedades deve ser o identificador de entrada de longo prazo do destinatário. Para garantir que cada destinatário inclua **a** propriedade PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)), passe a estrutura [ADRLIST](adrlist.md) descrevendo sua lista de destinatários no conteúdo do parâmetro  _lpAdrList_ em uma chamada para [IAddrBook::ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** começa o processamento ignorando as entradas na estrutura **ADRLIST** que já foram resolvidas, conforme indicado pela presença de um identificador de entrada na matriz **SPropValue** da estrutura [ADRENTRY](adrentry.md) correspondente. Em seguida, **ResolveName** atribui automaticamente identificadores de entrada único a dois tipos de destinatários: 
  
- Destinatários com um endereço formatado como um endereço da Internet
    
- Destinatários com um endereço formatado da seguinte forma:
    
     `displayname[address type:email address]`
    
Para todas as entradas restantes, **ResolveName** pesquisa no livro de endereços uma combinação exata no nome de exibição. **ResolveName** usa **a PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar o conjunto de contêineres a ser pesquisado e a ordem de pesquisa. O MAPI chama [o método IABContainer::ResolveNames](iabcontainer-resolvenames.md) de cada contêiner para tentar resolver todos os nomes. Como alguns **contêineres** não suportam **ResolveNames**, se o contêiner retornar MAPI_E_NO_SUPPORT, o MAPI aplicará uma restrição de propriedade PR_ANR ([PidTagAnr](pidtaganr-canonical-property.md)) em relação a sua tabela de conteúdo. Todos os contêineres do livro de endereços são necessários para dar suporte à resolução de nomes com essa restrição. Depois que todos os nomes são resolvidos, nenhuma outra chamada de contêiner é feita. Se todos os contêineres tiverem sido chamados, mas os nomes ambíguos ou não resolvidos permanecerem, o MAPI exibirá uma caixa de diálogo, se possível, para solicitar que o usuário resolva os nomes restantes.
  
A **PR_ANR** restrição corresponde ao valor da **propriedade PR_ANR** com o nome de exibição na estrutura **ADRLIST.** Limitar a exibição da tabela de conteúdo de um contêiner **com PR_ANR** restrição de propriedade faz com que o provedor de agendamento realize um tipo de pesquisa "melhor suposição", correspondendo à propriedade que faz sentido para o provedor. Por exemplo, um provedor de agendas sempre pode corresponder nomes na lista de destinatários com **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), enquanto outro pode permitir que um administrador selecione a propriedade.
  
 **Para definir uma PR_ANR restrição de propriedade em uma tabela de conteúdos de um contêiner de livro de endereços**
  
1. Crie uma [estrutura SRestriction](srestriction.md) conforme mostrado no código a seguir: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Chame o método [IMAPITable::Restrict](imapitable-restrict.md) da tabela de conteúdo, passando a **estrutura SRestriction** como o _parâmetro lpRestriction._ 
    

