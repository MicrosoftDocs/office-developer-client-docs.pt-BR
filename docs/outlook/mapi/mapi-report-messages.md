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
ms.openlocfilehash: addf93cadae418017a40ba448328d2e1fc1decf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767930"
---
# <a name="mapi-report-messages"></a>Mensagens de relatório MAPI

  
  
**Aplica-se a**: Outlook 
  
Relatar informações de status presente mensagens sobre uma mensagem ao remetente.
  
Há dois tipos gerais de mensagens de relatório:
  
- Leia os relatórios de status.
    
- Relatórios de status de entrega.
    
## <a name="read-status-reports"></a>Relatórios de Status de leitura

Relatórios de status de leitura são iniciados por provedores de armazenamento de mensagens através de uma chamada ao método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) e são enviados ao destinatário representado pelo identificador de entrada no **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) propriedade. Relatórios de status de leitura não são gerados automaticamente. aplicativos cliente que deseja recebê-las devem solicitar explicitamente-los.
  
Um relatório de leitura indica que o sinalizador de leitura de uma mensagem tiver sido definido, que pode ocorrer quando a mensagem é aberta, impressa, movida ou copiada. Se ou não um provedor de armazenamento de mensagem gera um relatório de leitura em resposta a uma movimentação ou cópia operação depende de onde a mensagem será. Se estiver sendo movido ou copiadas para outro repositório de mensagem, um ponto de relatório leitura provavelmente sempre ser enviadas. Se ele está sendo movido ou copiadas no armazenamento da mensagem atual, um relatório de leitura pode ou não pode ser enviado. 
  
Um relatório nonread indica que o sinalizador de leitura de uma mensagem não estiver definido e a mensagem não foi aberta tanto antes de ser colocada na pasta Itens excluídos ou antes de expirar um limite de tempo. Clientes podem chamar o método [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) para definir ou limpar o sinalizador de leitura da mensagem. 
  
## <a name="delivery-status-reports"></a>Relatórios de Status de entrega

Status de entrega é refletida em um relatório de entrega, que é enviado quando uma mensagem alcançou o receptor pretendido, e em um relatório de não entrega, que é enviado quando uma mensagem não poderia chegar a um destinatário. Relatórios de status de entrega são enviados ao destinatário representado pelo identificador de entrada na propriedade **PR_REPORT_ENTRYID** ou ao remetente se esta propriedade não estiver presente. 
  
Notificações de entrega são enviadas somente mediante solicitação e não incluir a mensagem original. NDRs são enviados automaticamente, a menos que uma solicitação for feita para suprimi-los. NDRs incluem a mensagem original como um anexo para habilitar o destinatário do relatório reenviar a mensagem no caso de qualquer item bloqueado a entrega não é mais um problema. A mensagem anexada se parece com o original, como ela se encontrava quando o método de [IMessage::SubmitMessage](imessage-submitmessage.md) foi acionado para enviá-la inicialmente. 
  
Um ou mais relatórios de status de entrega gerados por provedores de transporte quando eles chamam o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) . Uma lista de destinatários de uma mensagem é composto por provedores de transporte. Ou não um destinatário recebe um relatório e o tipo de relatório que é gerado depende dos seguintes fatores: 
  
- Notificações de entrega vá para destinatários que defina a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) como TRUE antes que a mensagem foi colocada no repositório de mensagem.
    
- NDRs vá para destinatários que não definido a propriedade **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) como FALSE. 
    
Quase todas as informações necessárias para exibir um relatório de não entrega está contida na tabela de destinatário da mensagem anexada. Algumas propriedades são provenientes do relatório em si. Para relatórios de entrega, as informações necessárias estão contidas na tabela de destinatário do relatório e, em algumas propriedades do relatório. 
  
Os relatórios são mensagens com classes de mensagem distintos, com base na classe da mensagem enviada. A maioria dos provedores de serviço usam uma convenção de nomenclatura no qual a classe da mensagem é composta de várias partes separadas por pontos. A primeira parte é "Relatório" e a última parte é uma constante que representa o tipo de relatório. Parte do meio é reservado para a classe da mensagem enviada. Por exemplo, como um relatório de entrega usa o DR constante, a classe de mensagem para uma entrega informar sobre um IPM. Mensagem de Observação seria **Report.IPM.Note.DR**.
  
A tabela a seguir mostra as constantes que representam os tipos de relatórios.
  
|**Tipo de relatório**|**Constante usada na classe da mensagem**|
|:-----|:-----|
|Read  <br/> |IPNRN  <br/> |
|Nonread  <br/> |IPNNRN  <br/> |
|Entrega  <br/> |RECUPERAÇÃO DE DESASTRES  <br/> |
|Não entrega  <br/> |NDR  <br/> |
   
Clientes Interactive podem exibir mensagens de relatório usando formulários padrão fornecidos pelo MAPI ou formulários personalizados que foram registrados com o Gerenciador de formulário para a classe de mensagem do relatório. Clientes que recebem um relatório de não entrega para um IPM. Mensagem de anotação, por exemplo, pode exibir o formulário padrão do MAPI que apresenta uma lista de destinatários com falha e um sugerido motivo da falha. O formulário também permite que o usuário reenviar a mensagem, se desejado. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

