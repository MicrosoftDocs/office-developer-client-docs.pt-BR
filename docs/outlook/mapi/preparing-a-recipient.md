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
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350670"
---
# <a name="preparing-a-recipient"></a>Preparar um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um aplicativo cliente prepara os destinatários convertendo seus identificadores de entrada de curto prazo para identificadores de entrada de longo prazo e possivelmente adicionando, alterando ou reordenando Propriedades. Você pode preparar destinatários que fazem parte de uma lista de destinatários para uma ou mais mensagens que não estão relacionadas a uma mensagem. Normalmente, os clientes chamam [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) diretamente para converter identificadores de entrada de curto prazo em identificadores de entrada de longo prazo para destinatários incluídos na caixa de diálogo endereço comum. Para destinatários associados a uma mensagem de saída, a preparação do destinatário é tratada pelo processo de resolução de nomes. 
  
Para preparar uma lista de destinatários, chame **IAddrBook::P reparerecips**. **PrepareRecips** aceita uma estrutura [das ADRLIST](adrlist.md) e uma lista de marcas de propriedade. A estrutura **das ADRLIST** contém os destinatários a serem preparados enquanto a lista de marcas de propriedade representa propriedades às quais cada destinatário deve suportar. **PrepareRecips** tenta colocar as propriedades incluídas na lista de marcas de propriedade no início da estrutura **das ADRLIST** . Se qualquer uma das propriedades na lista estiver ausente da estrutura **das ADRLIST** , o MAPI chamará o provedor de catálogo de endereços para fornecê-las. Se você precisar verificar identificadores de entrada de longo prazo, passe NULL para o parâmetro _lpSPropTagArray_ . 
  
Por exemplo, suponha que você está trabalhando com cinco destinatários. Todos os cinco destinatários aparecem na estrutura **das ADRLIST** com as seguintes propriedades na seguinte ordem: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Três outras propriedades estão incluídas na estrutura **das ADRLIST** para os primeiros dois destinatários. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Como todos os destinatários precisam ter suas primeiras três propriedades **PR_ADDRTYPE**, **PR_ENTRYID**e **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), crie uma matriz de marca de propriedade com essas propriedades e passe e a estrutura **das ADRLIST** como **PrepareRecips**. **PrepareRecips** chama o método **IMAPIProp::** GetProps de cada destinatário para recuperar o **PR_HOME_TELEPHONE_NUMBER** porque ele não faz parte da estrutura do **das ADRLIST** . Quando **PrepareRecips** retorna, a lista de destinatários representa uma lista mesclada de destinatários com as propriedades incluídas na estrutura **das ADRLIST** que aparecem primeiro para cada destinatário. 
  
A lista de destinatários para os destinatários 1 e 2 inclui propriedades na seguinte ordem:
  
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
    
A lista de destinatários para os destinatários 3, 4 e 5 inclui propriedades na seguinte ordem:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
Como alternativa para chamar **IAddrBook::P reparerecips** para trabalhar com propriedades, chame o método [IMAPIProp:](imapiprop-getprops.md) : GetProps de cada destinatário e, se necessário, o método [IMAPIProp::](imapiprop-setprops.md) SetProps. Quando somente um destinatário está envolvido, qualquer técnica é satisfatória. No enTanto, quando vários destinatários estão envolvidos, chamar **PrepareRecips** em vez dos métodos **IMAPIProp** poupa tempo e, se você estiver operando remotamente, várias chamadas de procedimento remoto. O **PrepareRecips** processa todos os destinatários em uma única chamada enquanto GetProps e SetProps fazem uma chamada para cada destinatário. **** **** 
  

