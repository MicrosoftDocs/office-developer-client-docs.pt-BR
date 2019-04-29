---
title: Propriedades do destinatário para relatórios de status de entrega
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b2e287e-1cf8-4b8f-b92c-a065ed264d02
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 784cac21aac5de18952f3768af9b8f189f604981
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411082"
---
# <a name="recipient-properties-for-delivery-status-reports"></a>Propriedades do destinatário para relatórios de status de entrega

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As propriedades a seguir estão presentes para relatórios de status de entrega para destinatários. **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) não é usado em notificações de falha na entrega. **PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md)) e **PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md)) são usados apenas em relatórios de não entrega.
  
**Título da tabela**

|**Propriedade**|**Como descriptografia**|
|:-----|:-----|
|**PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md))  <br/> |Contém a data e a hora em que a mensagem original foi entregue.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Contém o nome para exibição de um determinado objeto MAPI.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Contém um identificador de entrada MAPI usado para abrir e editar as propriedades de um objeto MAPI específico.  <br/> |
|**PR_NDR_DIAG_CODE** ([PidTagNonDeliveryReportDiagCode](pidtagnondeliveryreportdiagcode-canonical-property.md))  <br/> |Contém um código de diagnóstico que faz parte de uma notificação de falha na entrega.  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Contém uma cadeia de caracteres de texto que identifica a classe de mensagem definida pelo remetente, como IPM. Observação.  <br/> |
|**PR_NDR_REASON_CODE** ([PidTagNonDeliveryReportReasonCode](pidtagnondeliveryreportreasoncode-canonical-property.md))  <br/> |Contém um motivo codificado para a não entrega que faz parte de uma notificação de falha na entrega.  <br/> |
|**PR_ORIGINAL_DISPLAY_NAME** ([PidTagOriginalDisplayName](pidtagoriginaldisplayname-canonical-property.md))  <br/> |Contém o nome de exibição original de uma entrada copiada de um catálogo de endereços para um catálogo de endereços pessoal ou outro catálogo de endereços gravável.  <br/> |
|**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md))  <br/> |Contém o identificador de entrada original para uma entrada copiada de um catálogo de endereços para um catálogo de endereços pessoal ou outro catálogo de endereços gravável.  <br/> |
|**PR_ORIGINAL_SEARCH_KEY** ([PidTagOriginalSearchKey](pidtagoriginalsearchkey-canonical-property.md))  <br/> |Contém a chave de pesquisa original para uma entrada copiada de um catálogo de endereços para um catálogo de endereços pessoal ou outro catálogo de endereços gravável.  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Contém o tipo de destinatário para um destinatário de mensagem.  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |Contém texto opcional para um relatório gerado pelo sistema de mensagens.  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |Contém a data e hora em que o sistema de mensagens gerou um relatório.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Contém uma chave comparável à binária que identifica objetos correlacionados para uma pesquisa.  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Contém um valor usado para associar um ícone a uma linha específica de uma tabela.  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Contém o tipo de um objeto.  <br/> |
   

