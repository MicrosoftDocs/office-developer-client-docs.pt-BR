---
title: Preparar um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b4ccfb8cf8201a17993932acc4c0104ace80b94d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588717"
---
# <a name="preparing-a-recipient"></a>Preparar um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um aplicativo cliente prepara destinatários, convertendo seus identificadores de entrada de curto prazo aos identificadores de entrada de longo prazo e, possivelmente, adicionar, alterar ou reordenar propriedades. Você pode preparar destinatários que fazem parte de uma lista de destinatários de uma mensagem ou destinatários que não estão relacionados a uma mensagem. Normalmente, os clientes chame [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) diretamente para traduzir identificadores de entrada de curto prazo em longo prazo identificadores de entrada para destinatários incluídos na caixa de diálogo endereço comuns. Para que os destinatários que estão associados uma mensagem de saída, preparação do destinatário é tratada pelo processo de resolução de nome. 
  
Para preparar uma lista de destinatários, chame **IAddrBook::PrepareRecips**. **PrepareRecips** aceita uma estrutura [ADRLIST](adrlist.md) e uma lista das marcas de propriedade. A estrutura **ADRLIST** contém os destinatários para estar preparado enquanto a lista de marcas de propriedade representa propriedades que deve oferecer suporte a cada destinatário. **PrepareRecips** tenta colocar as propriedades que estão incluídas na lista de marca de propriedade, no início da estrutura **ADRLIST** . Se qualquer uma das propriedades na lista estão ausentes da estrutura de **ADRLIST** , MAPI chama o provedor de catálogo de endereços para fornecê-las. Se você só precisa procurar a longo prazo identificadores de entrada, passe NULL para o parâmetro _lpSPropTagArray_ . 
  
Por exemplo, suponha que você estiver trabalhando com cinco destinatários. Todos os destinatários de cinco aparecem na estrutura de **ADRLIST** com as seguintes propriedades na seguinte ordem: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Três outras propriedades estão incluídas na estrutura de **ADRLIST** para os dois primeiros destinatários. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Como todos os destinatários precisam ter como suas três primeiras propriedades **PR_ADDRTYPE**, **PR_ENTRYID**e **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), crie uma matriz de marca de propriedade com essas propriedades e passe ela e a estrutura **ADRLIST** para **PrepareRecips**. **PrepareRecips** chama o método de **IMAPIProp::GetProps** de cada destinatário para recuperar **PR_HOME_TELEPHONE_NUMBER** porque atualmente não faz parte da estrutura de **ADRLIST** . Quando **PrepareRecips** retorna, a lista de destinatários representa uma lista mesclada de destinatários com as propriedades incluídas na estrutura de **ADRLIST** aparecendo primeiro para cada destinatário. 
  
A lista de destinatários para destinatários 1 e 2 inclui propriedades na seguinte ordem:
  
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
    
A lista de destinatários para destinatários 3, 4 e 5 inclui propriedades na seguinte ordem:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Como alternativa para chamar **IAddrBook::PrepareRecips** para trabalhar com propriedades, chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) de cada destinatário e, se necessário, seu método [IMAPIProp::SetProps](imapiprop-setprops.md) . Quando somente um destinatário está envolvido, qualquer técnica é satisfatória. No entanto, quando vários destinatários estão envolvidos, chamar **PrepareRecips** ao invés os métodos **IMAPIProp** poupa tempo e, caso esteja operando remotamente, número de chamadas de procedimento remoto. **PrepareRecips** processa todos os destinatários em uma única chamada enquanto **GetProps** e **SetProps** fazem uma chamada para cada destinatário. 
  

