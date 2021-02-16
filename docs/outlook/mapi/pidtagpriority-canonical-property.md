---
title: Propriedade canônica PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339428"
---
# <a name="pidtagpriority-canonical-property"></a>Propriedade canônica PidTagPriority

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a prioridade relativa de uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PRIORITY  <br/> |
|Identificador:  <br/> |0x0026  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade e a **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) não devem ser confundidos. A importância indica um valor para os usuários, enquanto a prioridade indica a ordem ou a velocidade em que a mensagem deve ser enviada pelo software do sistema de mensagens. A prioridade mais alta geralmente indica um custo mais alto. Geralmente, a maior importância é associada a uma exibição diferente da interface do usuário.
  
A prioridade de uma mensagem de relatório deve ser a mesma que a prioridade da mensagem original que está sendo relatada.
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
PRIO_NONURGENT 
  
> A mensagem não é urgente.
    
PRIO_NORMAL 
  
> A mensagem tem prioridade normal.
    
PRIO_URGENT 
  
> A mensagem é urgente.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas em objetos de mensagem de email.
    
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

