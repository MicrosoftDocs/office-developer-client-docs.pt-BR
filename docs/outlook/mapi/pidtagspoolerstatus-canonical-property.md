---
title: Propriedade canônica PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: df52f668e91b707c0436b394186b27fdbb3a5dbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770066"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Propriedade canônica PidTagSpoolerStatus

  
  
**Aplica-se a**: Outlook 
  
Contém o status da mensagem com base nas informações que está disponíveis para o spooler MAPI.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Identificador:  <br/> |0x0E10  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é computada pelo MAPI em objetos de mensagem.
  
Essa propriedade é exibida no somente mensagens de entrada e está reservada em todos os outros casos. Indica se uma mensagem foi entregue ao local final ou se um provedor de fora do gancho mensagens potencialmente excluiu a mensagem enquanto reencaminhamento-lo.
  
Aplicativos cliente nunca devem definir essa propriedade. Para uma mensagem de entrada, um provedor de cliente ou serviço pode chamar [IMAPIProp::GetProps](imapiprop-getprops.md) sobre esta propriedade para determinar o status da mensagem. O valor S_OK indica que a mensagem foi entregue com êxito para o armazenamento de mensagens. O valor MAPI_E_OBJECT_DELETED indica que a mensagem foi excluída e nunca foi comprometida com o repositório. 
  
Provedores de armazenamento de mensagem devem oferecer suporte a essa propriedade em mensagens, tabelas de destinatários e a tabela de fila de saída. Clientes e provedores devem poder definir colunas na tabela de fila de saída e restringir com base nessa propriedade.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

