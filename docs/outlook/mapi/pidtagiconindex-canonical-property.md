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
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346617"
---
# <a name="pidtagiconindex-canonical-property"></a>Propriedade canônica PidTagIconIndex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um número que indica qual ícone usar ao exibir um grupo de objetos de email.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ICON_INDEX  <br/> |
|Identificador:  <br/> |0x1080  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade, se existir, é uma dica para o cliente. O cliente pode ignorar o valor dessa propriedade. 
  
|**Estado do item de email**|**Índice de ícone**|
|:-----|:-----|
|Novo email  <br/> |0xFFFFFFFF  <br/> |
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
|Entrega de email  <br/> |0x00000108  <br/> |
|Ler email  <br/> |0x00000109  <br/> |
|Nondelivery mail  <br/> |0x0000010A  <br/> |
|Email não lido  <br/> |0x0000010B  <br/> |
|Recall_S email  <br/> |0x0000010C  <br/> |
|Recall_F email  <br/> |0x0000010D  <br/> |
|Acompanhar emails  <br/> |0x0000010E  <br/> |
|Email de fora do escritório  <br/> |0x0000011B  <br/> |
|Recall mail  <br/> |0x0000011C  <br/> |
|Email rastreado  <br/> |0x00000130  <br/> |
|Contato  <br/> |0x00000200  <br/> |
|Lista de distribuição  <br/> |0x00000202  <br/> |
|Observação sticky azul  <br/> |0x00000300  <br/> |
|Observação sticky verde  <br/> |0x00000301  <br/> |
|Nota colada rosa  <br/> |0x00000302  <br/> |
|Observação sticky amarelo  <br/> |0x00000303  <br/> |
|Nota sticky branca  <br/> |0x00000304  <br/> |
|Compromisso de instância única  <br/> |0x00000400  <br/> |
|Compromisso recorrente  <br/> |0x00000401  <br/> |
|Reunião de instância única  <br/> |0x00000402  <br/> |
|Reunião recorrente  <br/> |0x00000403  <br/> |
|Solicitação de reunião  <br/> |0x00000404  <br/> |
|Aceitar  <br/> |0x00000405  <br/> |
|Recusar  <br/> |0x00000406  <br/> |
|Tentativly  <br/> |0x00000407  <br/> |
|Cancelamento  <br/> |0x00000408  <br/> |
|Atualização informacional  <br/> |0x00000409  <br/> |
|Tarefa/tarefa  <br/> |0x00000500  <br/> |
|Tarefa recorrente não atribuída  <br/> |0x00000501  <br/> |
|Tarefa do destinatário  <br/> |0x00000502  <br/> |
|Tarefa do atribuídor  <br/> |0x00000503  <br/> |
|Solicitação de tarefa  <br/> |0x00000504  <br/> |
|Aceitação da tarefa  <br/> |0x00000505  <br/> |
|Rejeição da tarefa  <br/> |0x00000506  <br/> |
|Conversa no diário  <br/> |0x00000601  <br/> |
|Mensagem de email do diário  <br/> |0x00000602  <br/> |
|Solicitação de reunião no diário  <br/> |0x00000603  <br/> |
|Resposta de reunião no diário  <br/> |0x00000604  <br/> |
|Solicitação de tarefa de diário  <br/> |0x00000606  <br/> |
|Resposta de tarefa de diário  <br/> |0x00000607  <br/> |
|Observação do diário  <br/> |0x00000608  <br/> |
|Fax de diário  <br/> |0x00000609  <br/> |
|Chamada telefônica de diário  <br/> |0x0000060A  <br/> |
|Carta de diário  <br/> |0x0000060C  <br/> |
|Diário do Microsoft Office Word  <br/> |0x0000060D  <br/> |
|Diário do Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Diário do Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|Diário do Microsoft Office Access  <br/> |0x00000610  <br/> |
|Documento do diário  <br/> |0x00000612  <br/> |
|Reunião no diário  <br/> |0x00000613  <br/> |
|Cancelamento de reunião no diário  <br/> |0x00000614  <br/> |
|Sessão remota de diário  <br/> |0x00000615  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas em objetos de mensagem de email.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas em contatos e listas de distribuição pessoais.
    
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

