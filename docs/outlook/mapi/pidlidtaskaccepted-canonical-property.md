---
title: Propriedade canônico de PidLidTaskAccepted
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7448768a0a35cbf53b481eab0571b405fead1544
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768688"
---
# <a name="pidlidtaskaccepted-canonical-property"></a>Propriedade canônico de PidLidTaskAccepted

  
  
**Aplica-se a**: Outlook 
  
Indica se um destinatário de tarefa respondeu a uma solicitação de tarefa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTaskAccepted  <br/> |
|Propriedade definida:  <br/> |PSETID_Task  <br/> |
|ID de longo (LID):  <br/> |0x00008108  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Coment�rios

O cliente define essa propriedade como FALSE para uma nova tarefa ou o cliente define essa propriedade como TRUE quando uma tarefa é aceita ou rejeitada. Se a propriedade for deixada não definida, um valor FALSE é assumido.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

