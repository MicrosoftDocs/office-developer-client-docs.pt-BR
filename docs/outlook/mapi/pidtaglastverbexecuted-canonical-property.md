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
ms.openlocfilehash: fe75a242772441b23d3aaa87fc57486d1f074914
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581654"
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

Essa propriedade pode ter um os seguintes valores:
  
|**Verbo**|**Valor da propriedade**|
|:-----|:-----|
|Postagem  <br/> |0x00000001  <br/> |
|Outro  <br/> |0x00000003  <br/> |
|Ler email  <br/> |0x00000100  <br/> |
|Email não lido  <br/> |0x00000101  <br/> |
|Emails enviados  <br/> |0x00000102  <br/> |
|Emails não enviados  <br/> |0x00000103  <br/> |
|Email de recebimento  <br/> |0x00000104  <br/> |
|Email respondido  <br/> |0x00000105  <br/> |
|Correio encaminhado  <br/> |0x00000106  <br/> |
|Email remoto  <br/> |0x00000107  <br/> |
|Confirmação de entrega  <br/> |0x00000108  <br/> |
|Confirmação de leitura  <br/> |0x00000109  <br/> |
|Confirmação de não entrega  <br/> |0x0000010A  <br/> |
|Confirmação nonread  <br/> |0x0000010B  <br/> |
|Email Recall_S  <br/> |0x0000010C  <br/> |
|Email Recall_F  <br/> |0x0000010D  <br/> |
|Acompanhamento de email  <br/> |0x0000010E  <br/> |
|Sem o email do Office  <br/> |0x0000011B  <br/> |
|Lembre-se de email  <br/> |0x0000011C  <br/> |
|Email controlada  <br/> |0x00000139  <br/> |
|Contato  <br/> |0x00000200  <br/> |
|Lista de distribuição  <br/> |0x00000201  <br/> |
|Nota, azul  <br/> |0x00000300  <br/> |
|Nota, verde  <br/> |0x00000301  <br/> |
|Nota, rosa  <br/> |0x00000302  <br/> |
|Nota, amarelo  <br/> |0x00000303  <br/> |
|Nota, branco  <br/> |0x00000304  <br/> |
|Compromisso de única instância  <br/> |0x00000400  <br/> |
|Compromisso recorrente  <br/> |0x00000401  <br/> |
|Reunião de ocorrência única  <br/> |0x00000402  <br/> |
|Reunião recorrente  <br/> |0x00000403  <br/> |
|Solicitação de reunião / completos de atualização  <br/> |0x00000404  <br/> |
|Aceitar  <br/> |0x00000405  <br/> |
|Recusar  <br/> |0x00000406  <br/> |
|Aceitar provisoriamente  <br/> |0x00000407  <br/> |
|Cancelamento  <br/> |0x00000408  <br/> |
|Atualização informativa  <br/> |0x00000409  <br/> |
|Atualização de tarefa/tarefa  <br/> |0x00000500  <br/> |
|Tarefa recorrente não atribuída  <br/> |0x00000501  <br/> |
|Tarefa da destinatário  <br/> |0x00000502  <br/> |
|Tarefa do cedente  <br/> |0x00000503  <br/> |
|Solicitação de Tarefa  <br/> |0x00000504  <br/> |
|Aceitação de tarefa  <br/> |0x00000505  <br/> |
|Rejeição de tarefa  <br/> |0x00000506  <br/> |
|Conversa de diário  <br/> |0x00000601  <br/> |
|Mensagem de Email do diário  <br/> |0x00000602  <br/> |
|Solicitação de reunião de diário  <br/> |0x00000603  <br/> |
|Resposta de reunião de diário  <br/> |0x00000604  <br/> |
|Solicitação de tarefa de diário  <br/> |0x00000606  <br/> |
|Resposta de tarefa de diário  <br/> |0x00000607  <br/> |
|Anotação do diário  <br/> |0x00000608  <br/> |
|Fax de diário  <br/> |0x00000609  <br/> |
|Chamada telefônica de diário  <br/> |0x0000060A  <br/> |
|Tarefa de diário  <br/> |0x0000060B  <br/> |
|Letra de diário  <br/> |0x0000060C  <br/> |
|Diário do Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Diário do Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Diário do Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Diário do Microsoft Office Access  <br/> |0x00000610  <br/> |
|Documento de diário  <br/> |0x00000612  <br/> |
|Reunião de diário  <br/> |0x00000613  <br/> |
|Cancelamento de reunião de diário  <br/> |0x00000614  <br/> |
|Sessão remota de diário  <br/> |0x00000615  <br/> |
|Novo email  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
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

