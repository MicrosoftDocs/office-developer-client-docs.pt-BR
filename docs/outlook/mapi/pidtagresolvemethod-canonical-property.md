---
title: Propriedade canônica PidTagResolveMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e67cbb113899487f489ef7235d92d1adfcb76163
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563636"
---
# <a name="pidtagresolvemethod-canonical-property"></a>Propriedade canônica PidTagResolveMethod

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o valor de resolução de conflito de uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOLVE_METHOD  <br/> |
|Identificador:  <br/> |0x3FE7  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade na pasta que contém a mensagem de resolução de conflito indicará como resolver o conflito. Essa propriedade não é necessária. No entanto, se ele estiver definido, os sinalizadores que não seja a seguir não devem estar presentes:
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0X00000000)  <br/> |Conflito resolver mensagem deve ser gerada.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0X00000001)  <br/> |Substitua a mensagem de destino com alterações atuais que está sendo aplicadas.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0X00000002)  <br/> |Não envie mensagem de notificação de conflito quando gerando conflito resolver a mensagem na pasta pública.  <br/> |
   
Um cliente ou servidor não deve gerar uma mensagem de conflito resolve para mensagens associadas. Essas mensagens devem ser resolvidas usando semântica **RESOLVE_METHOD_LAST_WRITER_WINS** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicos que são usadas em operações remotas.
    
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

