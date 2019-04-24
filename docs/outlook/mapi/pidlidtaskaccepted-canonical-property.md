---
title: Propriedade canônica PidLidTaskAccepted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0172bf0d69c3f345b592364be754f58c9e7a4420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331280"
---
# <a name="pidlidtaskaccepted-canonical-property"></a>Propriedade canônica PidLidTaskAccepted

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se um destinatário de tarefa respondeu a uma solicitação de tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskAccepted  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008108  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Comentários

O cliente define essa propriedade como FALSE para uma nova tarefa ou o cliente define essa propriedade como TRUE quando uma tarefa é aceita ou rejeitada. Se a propriedade for Left unfalse, um valor FALSE será usado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

