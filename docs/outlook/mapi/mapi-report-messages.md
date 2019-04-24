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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329740"
---
# <a name="mapi-report-messages"></a>Mensagens de relatório MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mensagens de relatório apresentam informações de status sobre uma mensagem para seu remetente.
  
Há dois tipos gerais de mensagens de relatórios:
  
- Ler relatórios de status.
    
- Relatórios de status de entrega.
    
## <a name="read-status-reports"></a>Ler relatórios de status

Os relatórios de status de leitura são iniciados por provedores de repositório de mensagens por meio de uma chamada para o método [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) e são enviados ao destinatário representado pelo identificador de entrada no **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)) Propriedades. Os relatórios de status de leitura não são gerados automaticamente; os aplicativos clientes que desejam recebê-los devem explicitamente solicitá-los.
  
Um relatório de leitura indica que o sinalizador de leitura de uma mensagem foi definido, o que pode ocorrer quando a mensagem é aberta, impressa, movida ou copiada. Se um provedor de repositório de mensagens gera ou não um relatório de leitura em resposta a uma operação de movimentação ou cópia depende de onde a mensagem está indo. Se ele estiver sendo movido ou copiado para outro repositório de mensagens, um relatório de leitura provavelmente sempre será enviado. Se ele estiver sendo movido ou copiado no repositório de mensagens atual, um relatório de leitura poderá ou não ser enviado. 
  
Um relatório não lido indica que o sinalizador de leitura de uma mensagem não está definido e que a mensagem não foi aberta antes de ser colocada na pasta itens excluídos ou antes da expiração de um limite de tempo. Os clientes podem chamar o método [IMessage:: SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) para definir ou desmarcar o sinalizador de leitura de uma mensagem. 
  
## <a name="delivery-status-reports"></a>Relatórios de status de entrega

O status de entrega é refletido em um relatório de entrega, que é enviado quando uma mensagem atinge seu destinatário desejado e, em um relatório de não entrega, que é enviado quando uma mensagem não conseguiu acessar um destinatário. Os relatórios de status de entrega são enviados para o destinatário representado pelo identificador de entrada na propriedade **PR_REPORT_ENTRYID** ou ao remetente se essa propriedade não estiver presente. 
  
Os relatórios de entrega são enviados apenas pela solicitação e não incluem a mensagem original. Os relatórios de não entrega são enviados automaticamente, a menos que uma solicitação seja suprimida. Os relatórios de não entrega incluem a mensagem original como um anexo para permitir que o destinatário do relatório reenvie a mensagem caso o bloqueio da entrega não seja mais um problema. A mensagem anexada se parece com o original como existia quando o método [IMessage:: SubmitMessage](imessage-submitmessage.md) foi chamado para enviá-lo inicialmente. 
  
Um ou mais relatórios de status de entrega são gerados por provedores de transporte quando chamam o método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) . Provedores de transporte compõem uma lista de destinatários para uma mensagem. Se um destinatário receberá ou não um relatório e o tipo de relatório gerado dependerá do seguinte: 
  
- Os relatórios de entrega vão para os destinatários que definem a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PIDTAGORIGINATORDELIVERYREPORTREQUESTED](pidtagoriginatordeliveryreportrequested-canonical-property.md)) como true antes da mensagem ser colocada no repositório de mensagens.
    
- Os relatórios de não entrega vão para destinatários que não definiram a propriedade **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PIDTAGORIGINATORNONDELIVERYREPORTREQUESTED](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) como false. 
    
Quase todas as informações necessárias para exibir um relatório de não entrega estão contidas na tabela de destinatários da mensagem anexada. Algumas propriedades são do próprio relatório. Para relatórios de entrega, as informações necessárias estão contidas na tabela de destinatários do relatório e em algumas propriedades de relatório. 
  
Relatórios são mensagens com classes de mensagens distintas, com base na classe da mensagem enviada. A maioria dos provedores de serviços usa uma Convenção de nomenclatura na qual a classe de mensagem é composta por várias partes separadas por pontos. A primeira parte é "Report" e a última parte é uma constante que representa o tipo de relatório. A parte intermediária é reservada para a classe da mensagem enviada. Por exemplo, como um relatório de entrega usa a constante DR, a classe de mensagem para um relatório de entrega sobre uma IPM. A mensagem de observação seria **Report. IPM. Note. Dr**.
  
A tabela a seguir mostra as constantes que representam os tipos de relatórios.
  
|**Tipo de relatório**|**Constante usada na classe de mensagem**|
|:-----|:-----|
|Leitura  <br/> |IPNRN  <br/> |
|Não leitura  <br/> |IPNNRN  <br/> |
|Entrega  <br/> |RECUPERAÇÃO  <br/> |
|Não entrega  <br/> |ENTREGA  <br/> |
   
Os clientes interAtivos podem exibir mensagens de relatório usando formulários padrão fornecidos por MAPI ou formulários personalizados que foram registrados com o Gerenciador de formulários para a classe de mensagens do relatório. Clientes que recebem um relatório de não entrega para IPM. Observação a mensagem, por exemplo, pode exibir o formulário MAPI padrão que apresenta uma lista de destinatários com falha e um motivo sugerido para a falha. O formulário também permite que o usuário reenvie a mensagem, se desejado. 
  
## <a name="see-also"></a>Confira também



[Mensagens MAPI](mapi-messages.md)

