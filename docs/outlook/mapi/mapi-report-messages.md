---
title: Mensagens de relatório MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 824eb670-16b7-49bf-9992-39fe0586a552
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aab5c76fb268729f1a50a33e4764905fe3d53405
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405762"
---
# <a name="mapi-report-messages"></a>Mensagens de relatório MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As mensagens de relatório apresentam informações de status sobre uma mensagem para seu remetente.
  
Há dois tipos gerais de mensagens de relatório:
  
- Ler relatórios de status.
    
- Relatórios de status de entrega.
    
## <a name="read-status-reports"></a>Ler relatórios de status

Os relatórios de status de leitura são iniciados por provedores de armazenamento de mensagens por meio de uma chamada para o método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) e enviados ao destinatário representado pelo identificador de entrada na propriedade **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)). Os relatórios de status de leitura não são gerados automaticamente; os aplicativos cliente que deseja recebê-los devem solicitá-los explicitamente.
  
Um relatório de leitura indica que o sinalizador de leitura de uma mensagem foi definido, o que pode ocorrer quando a mensagem é aberta, impressa, movida ou copiada. Se um provedor de armazenamento de mensagens gera ou não um relatório de leitura em resposta a uma operação de movimentação ou cópia depende de onde a mensagem está indo. Se ele estiver sendo movido ou copiado para outro armazenamento de mensagens, um relatório de leitura provavelmente sempre será enviado. Se ele estiver sendo movido ou copiado no armazenamento de mensagens atual, um relatório de leitura pode ou não ser enviado. 
  
Um relatório não lido indica que o sinalizador de leitura de uma mensagem não está definido e que a mensagem não foi aberta antes de ser colocada na pasta Itens Excluídos ou antes da expiração de um limite de tempo. Os clientes podem chamar o método [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) para definir ou limpar o sinalizador de leitura de uma mensagem. 
  
## <a name="delivery-status-reports"></a>Relatórios de Status de Entrega

O status de entrega é refletido em um relatório de entrega, que é enviado quando uma mensagem atinge seu destinatário pretendido e em um relatório de não entrega, que é enviado quando uma mensagem não conseguiu alcançar um destinatário. Relatórios de status de entrega são enviados ao destinatário representado pelo identificador de entrada na propriedade **PR_REPORT_ENTRYID** ou ao remetente se essa propriedade não estiver presente. 
  
Os relatórios de entrega são enviados apenas por solicitação e não incluem a mensagem original. Os relatórios de não entrega são enviados automaticamente, a menos que seja feita uma solicitação para suprimi-los. Os relatórios de não entrega incluem a mensagem original como um anexo para permitir que o destinatário do relatório reenda a mensagem caso o que tenha bloqueado a entrega não seja mais um problema. A mensagem anexada se parece com o original como existia quando o método [IMessage::SubmitMessage](imessage-submitmessage.md) foi chamado para enviá-la inicialmente. 
  
Um ou mais relatórios de status de entrega são gerados por provedores de transporte quando eles chamam o [método IMAPISupport::StatusRecips.](imapisupport-statusrecips.md) Os provedores de transporte compõem uma lista de destinatários de uma mensagem. Se um destinatário recebe ou não um relatório e o tipo de relatório gerado depende do seguinte: 
  
- Os relatórios de entrega vão para destinatários que definirem a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) como VERDADEIRO antes de a mensagem ser colocada no armazenamento de mensagens.
    
- Os relatórios não entregues vão para destinatários que não definiram a propriedade **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) como FALSE. 
    
Quase todas as informações necessárias para exibir um relatório de não entrega estão contidas na tabela de destinatários da mensagem anexada. Algumas propriedades são do próprio relatório. Para relatórios de entrega, as informações necessárias estão contidas na tabela de destinatários do relatório e em algumas propriedades do relatório. 
  
Os relatórios são mensagens com classes de mensagens distintas, com base na classe da mensagem enviada. A maioria dos provedores de serviços usa uma convenção de nomen por meio da qual a classe de mensagem é composta de várias partes separadas por pontos. A primeira parte é "Relatório" e a última parte é uma constante que representa o tipo de relatório. A parte intermediária é reservada para a classe da mensagem enviada. Por exemplo, como um relatório de entrega usa a dr constante, a classe de mensagem para um relatório de entrega sobre um IPM. A mensagem de anotação **seria Report.IPM.Note.DR.**
  
A tabela a seguir mostra as constantes que representam os tipos de relatórios.
  
|**Tipo de relatório**|**Constante usada na classe message**|
|:-----|:-----|
|Ler  <br/> |IPNRN  <br/> |
|Não lido  <br/> |IPNNRN  <br/> |
|Entrega  <br/> |DR  <br/> |
|Nondelivery  <br/> |NDR  <br/> |
   
Os clientes interativos podem exibir mensagens de relatório usando formulários padrão fornecidos por MAPI ou formulários personalizados que foram registrados com o gerenciador de formulários para a classe de mensagens do relatório. Clientes que recebem um relatório de não entrega de um IPM. Note message, for example, can display the standard MAPI form that presents a list of the failed recipients and a suggested reason for the failure. O formulário também permite que o usuário reende a mensagem, se desejado. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

