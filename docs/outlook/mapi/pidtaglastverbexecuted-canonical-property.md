---
title: Propriedade canônica PidTagLastVerbExecuted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastVerbExecuted
api_type:
- HeaderDef
ms.assetid: 502f0261-697f-41bf-8530-75e1d0f503e5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9abd4eb955428595ebe41ab9b2c661303ee2779a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279612"
---
# <a name="pidtaglastverbexecuted-canonical-property"></a>Propriedade canônica PidTagLastVerbExecuted

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o último verbo executado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_LAST_VERB_EXECUTED  <br/> |
|Identificador:  <br/> |0x1081  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Histórico  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter um dos seguintes valores:
  
|**Verb**|**Valor da propriedade**|
|:-----|:-----|
|Postagem  <br/> |0x00000001  <br/> |
|Outros  <br/> |0x00000003  <br/> |
|Ler email  <br/> |0x00000100  <br/> |
|Email não lido  <br/> |0x00000101  <br/> |
|Email enviado  <br/> |0x00000102  <br/> |
|Email não enviado  <br/> |0x00000103  <br/> |
|Email de recebimento  <br/> |0x00000104  <br/> |
|Email respondido  <br/> |0x00000105  <br/> |
|Email encaminhado  <br/> |0x00000106  <br/> |
|Email remoto  <br/> |0x00000107  <br/> |
|Confirmação de entrega  <br/> |0x00000108  <br/> |
|Confirmação de Leitura  <br/> |0x00000109  <br/> |
|Nondelivery Receipt  <br/> |0x0000010A  <br/> |
|Recibo não lido  <br/> |0x0000010B  <br/> |
|Recall_S email  <br/> |0x0000010C  <br/> |
|Recall_F email  <br/> |0x0000010D  <br/> |
|Acompanhar emails  <br/> |0x0000010E  <br/> |
|Email de fora do Escritório  <br/> |0x0000011B  <br/> |
|Recall mail  <br/> |0x0000011C  <br/> |
|Email rastreado  <br/> |0x00000139  <br/> |
|Contato  <br/> |0x00000200  <br/> |
|Lista de distribuição  <br/> |0x00000201  <br/> |
|Observação Sticky, Blue  <br/> |0x00000300  <br/> |
|Observação Sticky, Verde  <br/> |0x00000301  <br/> |
|Observação Sticky, Rosa  <br/> |0x00000302  <br/> |
|Observação Sticky, Amarelo  <br/> |0x00000303  <br/> |
|Observação Sticky, Branco  <br/> |0x00000304  <br/> |
|Compromisso de Instância Única  <br/> |0x00000400  <br/> |
|Compromisso Recorrente  <br/> |0x00000401  <br/> |
|Reunião de Instância Única  <br/> |0x00000402  <br/> |
|Reunião recorrente  <br/> |0x00000403  <br/> |
|Solicitação de Reunião/Atualização Completa  <br/> |0x00000404  <br/> |
|Aceitar  <br/> |0x00000405  <br/> |
|Recusar  <br/> |0x00000406  <br/> |
|Aceitar provisão  <br/> |0x00000407  <br/> |
|Cancelation  <br/> |0x00000408  <br/> |
|Atualização informacional  <br/> |0x00000409  <br/> |
|Atualização de tarefa/tarefa  <br/> |0x00000500  <br/> |
|Tarefa Recorrente Não Atribuída  <br/> |0x00000501  <br/> |
|Tarefa do destinatário  <br/> |0x00000502  <br/> |
|Tarefa do atribuídor  <br/> |0x00000503  <br/> |
|Solicitação de Tarefa  <br/> |0x00000504  <br/> |
|Aceitação da Tarefa  <br/> |0x00000505  <br/> |
|Rejeição da Tarefa  <br/> |0x00000506  <br/> |
|Conversa de diário  <br/> |0x00000601  <br/> |
|Mensagem de Email do Diário  <br/> |0x00000602  <br/> |
|Solicitação de Reunião no Diário  <br/> |0x00000603  <br/> |
|Resposta de Reunião no Diário  <br/> |0x00000604  <br/> |
|Solicitação de Tarefa de Diário  <br/> |0x00000606  <br/> |
|Resposta de tarefa de diário  <br/> |0x00000607  <br/> |
|Observação do Diário  <br/> |0x00000608  <br/> |
|Fax de Diário  <br/> |0x00000609  <br/> |
|Chamada telefônica de diário  <br/> |0x0000060A  <br/> |
|Tarefa de Diário  <br/> |0x0000060B  <br/> |
|Carta de Diário  <br/> |0x0000060C  <br/> |
|Diário do Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Diário do Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Diário do Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Diário do Microsoft Office Access  <br/> |0x00000610  <br/> |
|Documento do Diário  <br/> |0x00000612  <br/> |
|Reunião no Diário  <br/> |0x00000613  <br/> |
|Cancelamento de reunião no diário  <br/> |0x00000614  <br/> |
|Sessão remota de diário  <br/> |0x00000615  <br/> |
|Novo email  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
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

