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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344559"
---
# <a name="smtp-addresses"></a>Endereços SMTP

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O formato dos endereços de email SMTP é definido na RFC 822. Os componentes MAPI devem lidar com qualquer endereço compatível com o padrão. No enTanto, há uma forma específica de endereço RFC 822 que melhor codifica endereços MAPI:
  
 _Display-Name_ **\<** _email-endereço_**\>**
  
Os colchetes angulares são incluídos como literais. Os espaços em branco são comuns em nomes para exibição; Eles não precisam ser colocados entre aspas. Um endereço típico pode ter a seguinte aparência, que pertence a um dos coautores da RFC 1521:
  
Nathaniel Borenstein \<NSB@bellcore.com\>
  
Se o nome de exibição contiver caracteres com significado especial nos endereços SMTP, como \< ou @, o nome de exibição inteiro deverá ser colocado entre aspas duplas. No email de saída, se o comprimento total do endereço de email e o nome de exibição exceder 255 caracteres, o nome para exibição deverá ser Descartado.
  
As partes de um endereço SMTP mapeiam as propriedades MAPI da seguinte maneira:
  
|**Componente de endereço SMTP**|**Propriedade MAPI**|
|:-----|:-----|
| _Display-Name_ para todos os destinatários  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _exibir nome_ do campo de  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _Display-nome_ para o campo de remetente  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _email-endereço_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implícito, sempre "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Se não houver um nome de exibição para um endereço no email de entrada, o endereço de email inteiro deverá ser usado em seu lugar. O tipo de endereço é sempre SMTP.
  
As propriedades de destinatário são obtidas da tabela de destinatários da mensagem MAPI; as propriedades do remetente são obtidas da própria mensagem.
  

