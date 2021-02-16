---
title: Propriedade canônica PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331868"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Propriedade canônica PidTagContentUnreadCount

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o número de mensagens não lidas em uma pasta, conforme calculado pelo armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Identificador:  <br/> |0x3603  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade calculada pelo armazenamento de mensagens é usada para duas finalidades diferentes, porém relacionadas. Em um objeto de pasta MAPI, ele contém o número de mensagens em uma pasta. Em uma linha de título em tabelas MAPI categorizadas, ela contém o número de mensagens não associadas não lidas na categoria correspondente a essa linha de título.
  
Essa propriedade contém o número de mensagens na tabela de conteúdo da pasta para a qual o sinalizador MSGFLAG_READ não está definido na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). A **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contém a contagem total de mensagens para a pasta. O **PR_CONTENT_COUNT** e essa propriedade são somente leitura para clientes. 
  
Alguns aplicativos cliente exibem a linha de título de uma categoria de maneira diferente, dependendo do valor dessa propriedade. Por exemplo, um cliente pode exibir uma categoria que inclui mensagens não lidas em negrito. Essa propriedade não pode ser usada como uma categoria e uma tentativa de fazer isso resulta no MAPI_E_INVALID_PARAMETER valor retornado do método [IMAPITable::SortTable.](imapitable-sorttable.md) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo do Microsoft Exchange Server relacionadas.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Lida com operações de pasta.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclui operações permitidas para os objetos de tabela principais.
    
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

