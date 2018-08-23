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
ms.openlocfilehash: 3ddde5d206eb4be56ce6a7bae77eb00237f12a0f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584293"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Propriedade canônica PidTagRecipientType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tipo de destinatário para um destinatário de mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Identificador:  <br/> |0x0C15  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatário MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

O tipo de destinatário contido nesta propriedade consiste em um valor necessário e um sinalizador opcional.
  
Esta propriedade deve conter exatamente um dos seguintes valores:
  
MAPI_TO 
  
> O destinatário é primário (a) do destinatário. Os clientes são necessários para lidar com destinatários principais. Todos os outros tipos são opcionais.
    
MAPI_CC 
  
> O destinatário é um destinatário de cópia carbono (CC), um destinatário que recebe uma mensagem além dos destinatários principais.
    
MAPI_BCC 
  
> O destinatário é um destinatário de cópia oculta (Cco). Principal e cópia carbono destinatários estão cientes da existência de destinatários Cco. 
    
MAPI_P1 
  
> O destinatário não recebeu com êxito a mensagem na tentativa anterior. Este é um reenvio de uma transmissão anterior.
    
Além disso, o seguinte sinalizador pode ser definido:
  
MAPI_SUBMITTED 
  
> O destinatário já tiver recebido a mensagem e não precisa recebê-la novamente. Este é um reenvio de uma transmissão anterior. Esse sinalizador é definido em conjunto com os valores **MAPI_TO**, **MAPI_CC**e **MAPI_BCC** . 
    
O valor de MAPI_P1 e o sinalizador **MAPI_SUBMITTED** é usado quando uma mensagem está sendo retransmitida devido a não entrega a um ou mais dos destinatários pretendidos. Para este tipo de retransmissão, o cliente define **MAPI_SUBMITTED** em cada destinatário que não precisa novamente a mensagem, mas deve ser exibido na lista de destinatários. Para cada destinatário que não recebeu a mensagem anteriormente, o cliente retém o destinatário original com seu valor **PR_RECIPIENT_TYPE** inalterada, mas Além disso, envia uma cópia do destinatário com MAPI_P1 no lugar o valor original. Essa cópia, que é descartada antes da entrega real, força o destinatário para o envelope P1 e garante a retransmissão físico para que o destinatário. A propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) é definida como FALSE para destinatários MAPI_P1.
  
Quando um cliente exibe um formulário de reenvio, somente os destinatários MAPI_P1 estão visíveis. A menos que o usuário insere destinatários adicionais, quando a mensagem é entregue, a lista de destinatários é exibida exatamente como quando a mensagem foi enviada pela primeira vez. 
  
Os **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e as propriedades de **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) estão relacionadas ao tipo de destinatário. Quando um cliente chama **IMAPIProp::SaveChanges da mensagem** e há pelo menos um destinatário na lista de destinatários, o provedor de armazenamento de mensagem define essas propriedades da seguinte maneira: 
  
|**Propriedade**|**Descrição**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Definido como TRUE se um ou mais dos destinatários estão **MAPI_TO** destinatários.  <br/> |
|PR_DISPLAY_CC  <br/> |Definido como TRUE se um ou mais dos destinatários estão **MAPI_CC** destinatários.  <br/> |
| PR_DISPLAY_BCC  <br/> |Definido como TRUE se um ou mais dos destinatários estão **MAPI_BCC** destinatários.  <br/> |
   
Em x. 400, o envelope P1 ou entrega é as informações necessárias para enviar uma mensagem, incluindo propriedades de endereço do destinatário e qualquer sinalizadores de opção controlando a entrega e respostas. Envelope P2 ou exibição é as informações que geralmente é exibidas para cada destinatário que não seja o texto da mensagem. Ela normalmente inclui o assunto, importância, prioridade, sensibilidade e hora de envio, bem como os nomes dos destinatários primários e copiados. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagRecipientStatus](pidtagrecipientstatus-canonical-property.md)
  
[Propriedade canônica PidTagDisplayTo](pidtagdisplayto-canonical-property.md)
  
[Propriedade canônica PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)
  
[Propriedade canônica PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

