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
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331399"
---
# <a name="pidtagresolvemethod-canonical-property"></a>Propriedade canônica PidTagResolveMethod

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o valor de resolução de conflitos de uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOLVE_METHOD  <br/> |
|Identificador:  <br/> |0x3FE7  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade na pasta que contém a mensagem de resolução de conflitos indicará como resolver o conflito. Essa propriedade não é necessária. No entanto, se estiver definido, sinalizadores que não sejam os seguintes não devem estar presentes:
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0x00000000)  <br/> |A mensagem de resolução de conflitos deve ser gerada.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)  <br/> |Substituir a mensagem de destino com as alterações atuais aplicadas.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)  <br/> |Não envie mensagem de notificação de conflito ao gerar mensagem de resolução de conflito na pasta pública.  <br/> |
   
Um cliente ou servidor não deve gerar uma mensagem de resolução de conflito para mensagens associadas. Essas mensagens devem ser resolvidas usando **RESOLVE_METHOD_LAST_WRITER_WINS** semântica. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
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

