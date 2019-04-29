---
title: Acesso de Representante
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3d6a0eaf8ad125a0ae1ea3abb57e2aa57e0bdfe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427259"
---
# <a name="delegate-access"></a>Acesso de Representante

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Acesso de representante refere-se � capacidade do usu�rio para enviar uma mensagem como outro usu�rio ou receber uma mensagem para outro usu�rio. Acesso de representante � um recurso de independente do provedor de servi�o de MAPI que provedores de transporte podem suportar se eles selecionaram. No entanto, o provedor n�o � necess�ria para faz�-lo. Acesso de representante � valioso quando for necess�rio que um usu�rio pode enviar mensagens como ou filtrar mensagens de entrada para outro usu�rio ou quando um usu�rio deve acessar o armazenamento de mensagens de outro usu�rio. Antes de permitir que um usu�rio delegado para se conectar ao reposit�rio de outro usu�rio, o provedor de armazenamento de mensagem deve verificar se o usu�rio delegado tem a autoridade apropriada. 
  
Existem dois grupos de propriedades que s�o usados para oferecer suporte ao acesso de representante:
  
 **PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md)) 
  
Nas mensagens de sa�da, as propriedades de **PR_SENT_REPRESENTING** identificam o usu�rio de mensagens que deve agir como o remetente. Os clientes podem definir essas propriedades como uma op��o. Se as propriedades de **PR_SENT_REPRESENTING** n�o s�o definidas quando a mensagem atingir um provedor de transporte que suporte ao acesso de representante, � responsabilidade do provedor defini-las junto com as propriedades de **PR_SENDER**. 
  
Nas mensagens de entrada, as propriedades de **PR_RCVD_REPRESENTING** identificam o usu�rio que deve agir como o destinat�rio. Provedores de transporte respons�vel para entrega de mensagens do representante devem definir as propriedades de **PR_RCVD_REPRESENTING** tanto o **PR_RECEIVED_BY**. Clientes que est�o recebendo uma mensagem de representante devem copiar os valores das propriedades **PR_SENT_REPRESENTING** para as propriedades de **PR_RCVD_REPRESENTING** correspondentes. 
  
Por exemplo, suponha que John est� recebendo mensagens de Suzana enquanto Suzana est� de f�rias. As propriedades de **PR_RCVD_REPRESENTING** identificam John como destinat�rio representante. Quando John envia uma resposta a uma mensagem que ele recebeu para Suzana, as propriedades da mensagem **PR_SENDER** identificam John como o remetente. Porque John � representando Suzana, as propriedades de **PR_SENT_REPRESENTING** identificam Suzana. 
  
As mensagens recebidas de representante tratamento geralmente devem proporcionar essas mensagens como o usu�rio mensagens identificadas pelas propriedades **PR_SENT_REPRESENTING** e n�o como o usu�rio identificado pelas propriedades **PR_SENDER** de provedores de transporte. A exce��o a essa regra � quando for necess�rio corresponder os tipos de privil�gio e transporte de acesso. Nesse caso, um provedor de transporte pode escolher uma identidade de envio. 
  
Se as propriedades de **PR_SENT_REPRESENTING** n�o est�o dispon�veis para uma mensagem de entrada representante, o provedor de transporte manipula��o de entrega defina-los, usando os valores das propriedades **PR_SENDER** correspondentes. Se as propriedades de **PR_SENT_REPRESENTING** est�o dispon�veis, mas o provedor de transporte n�o oferece suporte para acesso de representante, ele pode usar as propriedades de **PR_SENDER** para entrega. 
  

