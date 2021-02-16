---
title: Preparando um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419874"
---
# <a name="preparing-a-recipient"></a>Preparando um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um aplicativo cliente prepara destinatários convertendo seus identificadores de entrada de curto prazo em identificadores de entrada de longo prazo e possivelmente adicionando, alterando ou reordenando propriedades. Você pode preparar destinatários que fazem parte de uma lista de destinatários para uma mensagem ou destinatários que não estão relacionados a uma mensagem. Normalmente, os clientes chamam [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) diretamente para converter identificadores de entrada de curto prazo em identificadores de entrada de longo prazo para destinatários incluídos na caixa de diálogo de endereço comum. Para destinatários associados a uma mensagem de saída, a preparação do destinatário é manipulada pelo processo de resolução de nomes. 
  
Para preparar uma lista de destinatários, chame **IAddrBook::P repareRecips**. **PrepareRecips** aceita uma estrutura [ADRLIST](adrlist.md) e uma lista de marcas de propriedade. A **estrutura ADRLIST** contém os destinatários a serem preparados, enquanto a lista de marca de propriedade representa as propriedades que cada destinatário deve suportar. **PrepareRecips** tenta colocar as propriedades incluídas na lista de marca de propriedade no início da estrutura **ADRLIST.** Se alguma das propriedades na lista estiver ausente da estrutura **ADRLIST,** o MAPI chamará o provedor de agendas para fornerí-las. Se você só precisar verificar se há identificadores de entrada de longo prazo, passe NULL para _o parâmetro lpSPropTagArray._ 
  
Por exemplo, suponha que você está trabalhando com cinco destinatários. Todos os cinco destinatários aparecem na estrutura **ADRLIST** com as seguintes propriedades na seguinte ordem: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Três outras propriedades estão incluídas na **estrutura ADRLIST** para os dois primeiros destinatários. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Como todos os destinatários precisam ter como suas três primeiras propriedades **PR_ADDRTYPE**, **PR_ENTRYID** e **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), crie uma matriz de marca de propriedade com essas propriedades e passe-a e a estrutura **ADRLIST** para **PrepareRecips**. **PrepareRecips** chama o método **IMAPIProp::GetProps**  de cada destinatário para recuperar PR_HOME_TELEPHONE_NUMBER porque ele não faz parte da estrutura **ADRLIST** no momento. Quando **PrepareRecips** retorna, a lista de destinatários representa uma lista mesclada de destinatários com as propriedades incluídas na estrutura **ADRLIST** que aparecem primeiro para cada destinatário. 
  
A lista de destinatários dos destinatários 1 e 2 inclui propriedades na seguinte ordem:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
8. **PR_ACCOUNT**
    
9. **PR_GIVEN_NAME**
    
10. **PR_SURNAME**
    
A lista de destinatários dos destinatários 3, 4 e 5 inclui propriedades na seguinte ordem:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Como alternativa à chamada **de IAddrBook::P repareRecips** para trabalhar com propriedades, chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) de cada destinatário e, se necessário, seu método [IMAPIProp::SetProps.](imapiprop-setprops.md) Quando apenas um destinatário está envolvido, qualquer técnica é satisfatória. No entanto, quando vários destinatários estão envolvidos, chamar **PrepareRecips** em vez dos métodos **IMAPIProp** economiza tempo e, se você estiver operando remotamente, muitas chamadas de procedimento remoto. **PrepareRecips** processa todos os destinatários em uma única chamada, enquanto **GetProps** e **SetProps** fazem uma chamada para cada destinatário. 
  

