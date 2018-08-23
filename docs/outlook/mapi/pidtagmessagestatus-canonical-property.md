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
ms.openlocfilehash: 626bd945851155c20850ee7f367ec6073ad57bc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570384"
---
# <a name="pidtagmessagestatus-canonical-property"></a>Propriedade canônica PidTagMessageStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask de 32 bits dos sinalizadores que define o status de uma mensagem em uma tabela de conteúdo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MSG_STATUS  <br/> |
|Identificador:  <br/> |0x0E17  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Uma mensagem pode existir em uma tabela de conteúdo e em uma ou mais tabelas de resultados de pesquisa, e cada instância da mensagem pode ter um status diferente. Essa propriedade não deve ser considerada uma propriedade em uma mensagem, mas uma coluna em uma tabela de conteúdo. 
  
Um aplicativo cliente pode definir um ou mais dos seguintes sinalizadores nessa propriedade: 
  
MSGSTATUS_ANSWERED 
  
> A mensagem foi respondida. 
    
MSGSTATUS_DELMARKED 
  
> A mensagem foi marcada para exclusão subsequente. 
    
MSGSTATUS_DRAFT 
  
> A mensagem está no status de revisão de rascunho. 
    
MSGSTATUS_HIDDEN 
  
> A mensagem deve ser suprimida da exibe de pasta dos destinatários. 
    
MSGSTATUS_HIGHLIGHTED 
  
> A mensagem é realçado em exibições de pasta dos destinatários. 
    
MSGSTATUS_REMOTE_DELETE 
  
> A mensagem foi marcada para exclusão na loja remota de mensagens sem baixar no cliente local. 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> A mensagem foi marcada para download a partir do armazenamento de mensagens remoto no cliente local. 
    
MSGSTATUS_TAGGED 
  
> A mensagem foram marcada para uma finalidade definida pelo cliente.
    
Os sinalizadores **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**e **MSGSTATUS_TAGGED** são definidos pelo cliente. Provedores de transporte e o repositório passam esses bits sem qualquer ação. 
  
Os clientes podem interpretar esses valores de qualquer forma que é apropriada para seus aplicativos. Uma maneira que muitos clientes usam essa propriedade é para exibir mensagens marcadas para exclusão com um ícone de representante. 
  
Um cliente remoto visualizador pode definir **MSGSTATUS_REMOTE_DELETE** ou **MSGSTATUS_REMOTE_DOWNLOAD** em mensagens na pasta cabeçalho apresentada a ele pelo provedor de transporte remoto. O aplicativo cliente pode examinar cada cabeçalho da mensagem nesta pasta para determinar se a mensagem deve ser baixada ou excluída ao armazenamento de mensagens remoto. Ele usa o método [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) para definir o sinalizador apropriado. **SetMessageStatus** é a única maneira para definir qualquer um dos sinalizadores nessa propriedade; o método [IMAPIProp::SetProps](imapiprop-setprops.md) não pode ser usado. Para recuperar essa propriedade, os clientes chamar [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) em vez de [IMAPIProp::GetProps](imapiprop-getprops.md).
  
Bits 16 a 31 (0x10000 por meio de 0x80000000) dessa propriedade estarão disponíveis para uso pelo aplicativo cliente interpessoais mensagens (IPM). Todos os outros bits são reservados para uso pelo MAPI; aqueles não definido na tabela anterior devem ser definidas inicialmente como zero e subsequentemente não foi alteradas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMAPITable::QueryRows](imapitable-queryrows.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

