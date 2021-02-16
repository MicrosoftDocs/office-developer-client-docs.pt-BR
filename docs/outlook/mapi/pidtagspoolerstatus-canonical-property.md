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
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408674"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Propriedade canônica PidTagSpoolerStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o status da mensagem com base nas informações disponíveis para o spooler MAPI.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Identificador:  <br/> |0x0E10  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI não transmitível  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é calculada por MAPI em objetos de mensagem.
  
Essa propriedade aparece somente em mensagens de entrada e é reservada em todos os outros casos. Ele indica se uma mensagem foi entregue ou não ao seu local final ou se um provedor de gancho de mensagens potencialmente excluiu a mensagem enquanto a redirecionava.
  
Os aplicativos cliente nunca devem definir essa propriedade. Para uma mensagem de entrada, um cliente ou provedor de serviços pode chamar [IMAPIProp::GetProps](imapiprop-getprops.md) nessa propriedade para determinar o status da mensagem. O valor S_OK indica que a mensagem foi entregue com êxito ao armazenamento de mensagens. O valor MAPI_E_OBJECT_DELETED indica que a mensagem foi excluída e nunca foi comprometida com o armazenamento. 
  
Os provedores de armazenamento de mensagens devem dar suporte a essa propriedade em mensagens, tabelas de destinatários e na tabela de filas de saída. Os clientes e provedores devem ser capazes de definir colunas na tabela de filas de saída e restringir com base nessa propriedade.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

