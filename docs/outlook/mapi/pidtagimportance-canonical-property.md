---
title: Propriedade canônica PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327920"
---
# <a name="pidtagimportance-canonical-property"></a>Propriedade canônica PidTagImportance

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que indica a opinião do remetente da mensagem sobre a importância de uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IMPORTANCE  <br/> |
|Identificador:  <br/> |0x0017  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade e a **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) não devem ser confundidos. A importância indica um valor para os usuários, enquanto a prioridade indica a ordem ou a velocidade em que a mensagem deve ser enviada pelo software do sistema de mensagens. A prioridade mais alta geralmente indica um custo mais alto. Geralmente, a maior importância é associada a uma exibição diferente da interface do usuário. 
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
IMPORTANCE_LOW 
  
> A mensagem tem baixa importância.
    
IMPORTANCE_HIGH 
  
> A mensagem tem alta importância.
    
IMPORTANCE_NORMAL 
  
> A mensagem tem importância normal.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
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

