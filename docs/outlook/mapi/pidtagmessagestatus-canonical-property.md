---
title: Propriedade canônica PidTagMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355717"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Propriedade canônica PidTagMessageStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits de 32 bits de sinalizadores que define o status de uma mensagem em uma tabela de conteúdo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MSG_STATUS  <br/> |
|Identificador:  <br/> |0x0E17  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Uma mensagem pode existir em um índice de conteúdo e em uma ou mais tabelas de resultados de pesquisa, e cada instância da mensagem pode ter um status diferente. Essa propriedade não deve ser considerada uma propriedade em uma mensagem, mas uma coluna em uma tabela de conteúdo. 
  
Um aplicativo cliente pode definir um ou mais dos seguintes sinalizadores nesta propriedade: 
  
MSGSTATUS_ANSWERED 
  
> A mensagem foi respondida. 
    
MSGSTATUS_DELMARKED 
  
> A mensagem foi marcada para exclusão subsequente. 
    
MSGSTATUS_DRAFT 
  
> A mensagem está no status de revisão de rascunho. 
    
MSGSTATUS_HIDDEN 
  
> A mensagem deve ser suprimida na exibição da pasta dos destinatários. 
    
MSGSTATUS_HIGHLIGHTED 
  
> A mensagem deve ser realçada nas exibições da pasta dos destinatários. 
    
MSGSTATUS_REMOTE_DELETE 
  
> A mensagem foi marcada para exclusão no armazenamento de mensagens remoto sem ser baixada para o cliente local. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> A mensagem foi marcada para download do armazenamento de mensagens remoto para o cliente local. 
    
MSGSTATUS_TAGGED 
  
> A mensagem foi marcada para uma finalidade definida pelo cliente.
    
Os **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED** e MSGSTATUS_TAGGED são  definidos pelo cliente. Os provedores de transporte e armazenamento passam esses bits sem qualquer ação. 
  
Os clientes podem interpretar esses valores de qualquer maneira que seja apropriado para seus aplicativos. Uma maneira pela qual muitos clientes usam essa propriedade é exibir mensagens marcadas para exclusão com um ícone representativo. 
  
Um cliente de visualizador remoto pode MSGSTATUS_REMOTE_DELETE ou **MSGSTATUS_REMOTE_DOWNLOAD** mensagens na pasta de header apresentadas a ele pelo provedor de transporte remoto.  O aplicativo cliente pode examinar cada header de mensagem nessa pasta para determinar se a mensagem deve ser baixada ou excluída no armazenamento de mensagens remoto. Em seguida, ele usa [o método IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) para definir o sinalizador apropriado. **SetMessageStatus** é a única maneira de definir qualquer um dos sinalizadores nesta propriedade; o [método IMAPIProp::SetProps](imapiprop-setprops.md) não pode ser usado. Para recuperar essa propriedade, os clientes chamam [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) em vez de [IMAPIProp::GetProps](imapiprop-getprops.md).
  
Os bits de 16 a 31 (0x10000 0x80000000) dessa propriedade estão disponíveis para uso pelo aplicativo cliente de mensagem interpersonal (IPM). Todos os outros bits são reservados para uso por MAPI; aqueles não definidos na tabela anterior devem ser inicialmente definidos como zero e não alterados posteriormente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

