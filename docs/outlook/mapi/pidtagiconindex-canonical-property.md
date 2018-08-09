---
title: Propriedade canônica PidTagIconIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 83ab01363d478d197286bfa8f7b5b092a7ffd5a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769326"
---
# <a name="pidtagiconindex-canonical-property"></a>Propriedade canônica PidTagIconIndex

  
  
**Aplica-se a**: Outlook 
  
Contém um número que indica qual ícone a ser usado ao exibir um grupo de objetos de email.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ICON_INDEX  <br/> |
|Identificador:  <br/> |0x1080  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade, se ela existir, é uma dica ao cliente. O cliente pode ignorar o valor dessa propriedade. 
  
|**Estado de item de email**|**Índice do ícone**|
|:-----|:-----|
|Novo email  <br/> |0xFFFFFFFF  <br/> |
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
|Email de entrega  <br/> |0x00000108  <br/> |
|Ler email  <br/> |0x00000109  <br/> |
|Email de não entrega  <br/> |0x0000010A  <br/> |
|Email nonread  <br/> |0x0000010B  <br/> |
|Email Recall_S  <br/> |0x0000010C  <br/> |
|Email Recall_F  <br/> |0x0000010D  <br/> |
|Acompanhamento de email  <br/> |0x0000010E  <br/> |
|Sem o email do office  <br/> |0x0000011B  <br/> |
|Lembre-se de email  <br/> |0x0000011C  <br/> |
|Email controlada  <br/> |0x00000130  <br/> |
|Contato  <br/> |0x00000200  <br/> |
|Lista de distribuição  <br/> |0x00000202  <br/> |
|Azul nota  <br/> |0x00000300  <br/> |
|Verde nota  <br/> |0x00000301  <br/> |
|Rosa nota  <br/> |0x00000302  <br/> |
|Amarelo nota  <br/> |0x00000303  <br/> |
|White nota  <br/> |0x00000304  <br/> |
|Compromisso de única instância  <br/> |0x00000400  <br/> |
|Compromisso recorrente  <br/> |0x00000401  <br/> |
|Reunião de ocorrência única  <br/> |0x00000402  <br/> |
|Reunião recorrente  <br/> |0x00000403  <br/> |
|Solicitação de reunião  <br/> |0x00000404  <br/> |
|Aceitar  <br/> |0x00000405  <br/> |
|Recusar  <br/> |0x00000406  <br/> |
|Tentativly  <br/> |0x00000407  <br/> |
|Cancelamento  <br/> |0x00000408  <br/> |
|Atualização informativa  <br/> |0x00000409  <br/> |
|Tarefa/tarefa  <br/> |0x00000500  <br/> |
|Tarefa recorrente não atribuída  <br/> |0x00000501  <br/> |
|Tarefa do destinatário  <br/> |0x00000502  <br/> |
|Tarefa do cedente  <br/> |0x00000503  <br/> |
|Solicitação de tarefa  <br/> |0x00000504  <br/> |
|Aceitação de tarefa  <br/> |0x00000505  <br/> |
|Rejeição de tarefa  <br/> |0x00000506  <br/> |
|Conversa de diário  <br/> |0x00000601  <br/> |
|Mensagem de email do diário  <br/> |0x00000602  <br/> |
|Solicitação de reunião de diário  <br/> |0x00000603  <br/> |
|Resposta de reunião de diário  <br/> |0x00000604  <br/> |
|Solicitação de tarefa de diário  <br/> |0x00000606  <br/> |
|Resposta de tarefa de diário  <br/> |0x00000607  <br/> |
|Anotação do diário  <br/> |0x00000608  <br/> |
|Fax de diário  <br/> |0x00000609  <br/> |
|Chamada telefônica de diário  <br/> |0x0000060A  <br/> |
|Letra de diário  <br/> |0x0000060C  <br/> |
|Diário do Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Diário do Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Diário do Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Diário do Microsoft Office Access  <br/> |0x00000610  <br/> |
|Documento de diário  <br/> |0x00000612  <br/> |
|Reunião de diário  <br/> |0x00000613  <br/> |
|Cancelamento de reunião de diário  <br/> |0x00000614  <br/> |
|Sessão remota de diário  <br/> |0x00000615  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em contatos e listas de distribuição pessoal.
    
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

