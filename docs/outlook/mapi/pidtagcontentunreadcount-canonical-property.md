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
ms.openlocfilehash: b15dd467b7418ea10d384183dc32284924a90212
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581073"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Propriedade canônica PidTagContentUnreadCount

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o número de mensagens não lidas em uma pasta, como computado pelo armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Identificador:  <br/> |0x3603  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade computada pelo armazenamento de mensagens é usada para dois diferentes, embora relacionado, fins. Em um objeto de pasta MAPI, ele contém o número de mensagens em uma pasta. Em uma linha de cabeçalho nas tabelas MAPI categorizadas, ele contém o número de mensagens não lidas não associado na categoria correspondente para essa linha de título.
  
Essa propriedade contém o número de mensagens na tabela de conteúdo de pasta para o qual o sinalizador MSGFLAG_READ não está definido na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). A propriedade **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contém a contagem total de mensagens para a pasta. O **PR_CONTENT_COUNT** e essa propriedade são somente leitura aos clientes. 
  
Alguns aplicativos cliente exibem a linha do cabeçalho de uma categoria de forma diferente, dependendo do valor dessa propriedade. Por exemplo, um cliente pode exibir uma categoria que inclui mensagens não lidas em negrito. Essa propriedade não pode ser usada como uma categoria e uma tentativa para isso resulta em que o valor MAPI_E_INVALID_PARAMETER sendo retornado pelo método [IMAPITable:: SortTable](imapitable-sorttable.md) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Trata as operações de pasta.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclui as operações permitidas para os objetos de tabela principal.
    
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

