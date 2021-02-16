---
title: Endereços SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419622"
---
# <a name="smtp-addresses"></a>Endereços SMTP

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O formato dos endereços de email SMTP é definido na RFC 822. Os componentes MAPI devem lidar com qualquer endereço que seja de acordo com esse padrão. No entanto, há uma forma específica de endereço RFC 822 que codifica melhor os endereços MAPI:
  
 _display-name_ **\<** _email-address_**\>**
  
Os colchetes angulares são incluídos como literais. Espaços em branco são comuns em nomes de exibição; eles não precisam ser entre aspas. Um endereço típico pode se parecer com este, que pertence a um dos coautores da RFC 1521:
  
Rúl Borenstein \< nsb@bellcore.com\>
  
Se o nome de exibição contiver caracteres que tenham significado especial em endereços SMTP, como ou @, todo o nome de exibição deverá estar entre \< aspas duplas. No email de saída, se o tamanho total do endereço de email mais o nome de exibição exceder 255 caracteres, o nome de exibição deverá ser descartado.
  
As partes de um mapa de endereço SMTP em propriedades MAPI da seguinte forma:
  
|**Componente de endereço SMTP**|**Propriedade MAPI**|
|:-----|:-----|
| _display-name_ para todos os destinatários  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _display-name_ for From field  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _display-name_ para o campo Remetente  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _email-address_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implícito, sempre "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Se não houver um nome de exibição para um endereço no email de entrada, todo o endereço de email deverá ser usado. O tipo de endereço é sempre SMTP.
  
As propriedades de destinatário são retiradas da tabela de destinatários da mensagem MAPI; as propriedades do remetente são retiradas da mensagem em si.
  

