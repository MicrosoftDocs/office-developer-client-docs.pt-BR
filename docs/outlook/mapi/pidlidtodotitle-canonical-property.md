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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339939"
---
# <a name="pidlidtodotitle-canonical-property"></a>Propriedade canônica PidLidToDoTitle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém texto especificado pelo usuário para identificar esse objeto de mensagem em uma lista de a fazer consolidada.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidToDoTitle  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A4  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Tarefas  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não deve ser definida em uma tarefa. Para indicar uma propriedade vazia, não de definida como a cadeia de caracteres de comprimento zero; em vez disso, exclua-a. 
  
Ao sinalizar um objeto de mensagem e a propriedade não existir, um cliente deve gravar o valor de **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) para essa propriedade.
  
Em uma lista de coisas a fazer consolidada, se essa propriedade não existir, um cliente deverá substituir o valor da propriedade **PR_NORMALIZED_SUBJECT** ao exibir essa propriedade na lista de a fazer. 
  
Em um objeto de mensagem de rascunho, se o cliente implementa sinalizadores de remetente, essa propriedade deve ser definida com o mesmo valor que **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas à sinalização.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
  
[Propriedade can�nico de PidLidFlagRequest](pidlidflagrequest-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

