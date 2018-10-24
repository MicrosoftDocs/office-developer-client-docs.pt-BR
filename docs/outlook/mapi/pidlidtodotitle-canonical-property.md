---
title: Propriedade canônica PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397580"
---
# <a name="pidlidtodotitle-canonical-property"></a>Propriedade canônica PidLidToDoTitle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o texto especificáveis de usuário para identificar este objeto de mensagem em uma lista de tarefas pendentes consolidada.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidToDoTitle  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A4  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não deve ser definida em uma tarefa. Para indicar uma propriedade vazia, não definir essa propriedade para a cadeia de caracteres de comprimento zero, mas, em vez disso, excluí-la. 
  
Quando um objeto de mensagem e a propriedade de sinalização não existe, um cliente deve gravar o valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) essa propriedade.
  
Em uma lista de tarefas pendentes consolidada, se essa propriedade não existir, um cliente deve substituir o valor da propriedade **PR_NORMALIZED_SUBJECT** ao exibir essa propriedade na lista de tarefas pendentes. 
  
Em um objeto de mensagem de rascunho, se o cliente implementa sinalizadores de remetente, essa propriedade deve ser definida com o mesmo valor **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece as definições do conjunto de propriedades e referências para relacionados especificações de protocolo do Exchange Server
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas a sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedade canônico de PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
  
[Propriedade canônica PidLidFlagRequest](pidlidflagrequest-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

