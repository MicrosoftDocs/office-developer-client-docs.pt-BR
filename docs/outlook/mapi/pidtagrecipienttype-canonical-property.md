---
title: Propriedade canônica PidTagRecipientType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355255"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Propriedade canônica PidTagRecipientType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tipo de destinatário de um destinatário da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Identificador:  <br/> |0x0C15  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatário MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

O tipo de destinatário contido nessa propriedade consiste em um valor obrigatório e um sinalizador opcional.
  
Essa propriedade deve conter exatamente um dos seguintes valores:
  
MAPI_TO 
  
> O destinatário é um destinatário principal (Para). Os clientes são necessários para lidar com destinatários primários. Todos os outros tipos são opcionais.
    
MAPI_CC 
  
> O destinatário é um destinatário com cópia carbono (CC), um destinatário que recebe uma mensagem além dos destinatários primários.
    
MAPI_BCC 
  
> O destinatário é um destinatário com cópia carbono (Cc). Os destinatários de cópia primária e carbono não estão cientes da existência de destinatários Cc. 
    
MAPI_P1 
  
> O destinatário não recebeu com êxito a mensagem na tentativa anterior. Este é um resend de uma transmissão anterior.
    
Além disso, o sinalizador a seguir pode ser definido:
  
MAPI_SUBMITTED 
  
> O destinatário já recebeu a mensagem e não precisa recebê-la novamente. Este é um resend de uma transmissão anterior. Esse sinalizador é definido em conjunto com os **MAPI_TO,** **MAPI_CC** e **MAPI_BCC** valores. 
    
O MAPI_P1 e o **sinalizador MAPI_SUBMITTED** são usados quando uma mensagem está sendo retransmitida devido a um ou mais dos destinatários pretendidos. Para essa retransmissão,  o cliente define MAPI_SUBMITTED em todos os destinatários que não precisam da mensagem novamente, mas que devem ser exibidos na lista de destinatários. Para cada destinatário que não recebeu a mensagem anteriormente, o cliente mantém o destinatário original com seu valor **de PR_RECIPIENT_TYPE** inalterado, mas, além disso, envia uma cópia do destinatário com MAPI_P1 no lugar do valor original. Essa cópia, que é descartada antes da entrega real, força o destinatário no envelope P1 e garante a retransmissão física para esse destinatário. A **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) é definida como FALSE para MAPI_P1 destinatários.
  
Quando um cliente exibe um formulário de reend, somente os MAPI_P1 destinatários ficam visíveis. A menos que o usuário insira destinatários adicionais, quando a mensagem é entregue, a lista de destinatários aparece exatamente como era quando a mensagem foi enviada pela primeira vez. 
  
As **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) estão relacionadas ao tipo de destinatário. Quando um cliente chama o **IMAPIProp::SaveChanges** de uma mensagem e há pelo menos um destinatário na lista de destinatários, o provedor de armazenamento de mensagens define essas propriedades da seguinte forma: 
  
|**Propriedade**|**Descrição**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |De definida como TRUE se um ou mais dos destinatários **MAPI_TO** destinatários.  <br/> |
|PR_DISPLAY_CC  <br/> |De definida como TRUE se um ou mais dos destinatários **MAPI_CC** destinatários.  <br/> |
| PR_DISPLAY_BCC  <br/> |De definida como TRUE se um ou mais dos destinatários **MAPI_BCC** destinatários.  <br/> |
   
No X.400, o P1 ou o envelope de entrega são as informações necessárias para entregar uma mensagem, incluindo as propriedades de endereço do destinatário e quaisquer sinalizadores de opção que controlam a entrega e as respostas. O envelope P2 ou de exibição é a informação normalmente exibida para cada destinatário que não seja o texto da mensagem em si. Normalmente, ele inclui o assunto, a importância, a prioridade, a sensibilidade e o tempo de envio, bem como os nomes dos destinatários principais e copiados. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagRecipientStatus](pidtagrecipientstatus-canonical-property.md)
  
[Propriedade canônica PidTagDisplayTo](pidtagdisplayto-canonical-property.md)
  
[Propriedade canônica PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)
  
[Propriedade canônica PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

