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
ms.openlocfilehash: 9bc77e3226066dc88bbaf4f4efc324825add8919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770462"
---
# <a name="smtp-addresses"></a>Endereços SMTP

  
  
**Aplica-se a**: Outlook 
  
O formato dos endereços de email SMTP é definido no RFC 822. Componentes MAPI devem lidar com qualquer endereço compatível com esse padrão. No entanto, há um determinado formato de endereço de RFC 822 que melhor codifica endereços MAPI:
  
 _nome para exibição_ **\<** _endereço de email_**\>**
  
Os colchetes angulares são incluídos como literais. Espaços em branco são comuns em nomes de exibição; eles não precisam ser citados. Um endereço típico pode parecer como este, que pertence a um dos coauthors do RFC 1521:
  
Nathaniel Borenstein \<nsb@bellcore.com\>
  
Se o nome de exibição contém caracteres que têm um significado especial em endereços SMTP, tais como \< ou @, o nome para exibição inteira deve estar entre aspas duplas. Em mensagens de saída, se o comprimento total do endereço de email mais exibir nome exceda 255 caracteres, o nome para exibição deve ser descartado.
  
As partes de um endereço SMTP ser mapeadas para propriedades MAPI da seguinte maneira:
  
|**Componente de endereço de SMTP**|**Propriedade MAPI**|
|:-----|:-----|
| _nome de exibição_ para todos os destinatários  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
| _nome de exibição_ para do campo  <br/> |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
| _nome de exibição_ para o campo de remetente  <br/> |**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |
| _endereço de email_ <br/> |**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |
|implícita, sempre "SMTP"  <br/> |**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |
   
Se não houver nenhum nome de exibição para um endereço de email de entrada, o endereço de email inteira deve ser usado. O tipo de endereço é sempre SMTP.
  
Propriedades de destinatário são obtidas da tabela de destinatário da mensagem MAPI; Propriedades do remetente são utilizadas da própria mensagem.
  

