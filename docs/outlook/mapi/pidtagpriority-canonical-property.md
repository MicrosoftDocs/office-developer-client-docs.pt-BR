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
ms.openlocfilehash: 1e69211c15a3a05b3396dc1510483fddafe3faeb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588605"
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

Essa propriedade e a propriedade **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) não devem ser confundidos. Prioridade indica um valor para os usuários, enquanto a prioridade indica a ordem ou a velocidade na qual a mensagem deve ser enviada pelo software do sistema de mensagens. Geralmente, a prioridade mais alta indica um alto custo. Prioridade mais alta geralmente é associada uma exibição diferentes pela interface do usuário.
  
A prioridade de uma mensagem de relatório deve ser o mesmo que a prioridade da mensagem original serem reportada.
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
PRIO_NONURGENT 
  
> A mensagem não é urgente.
    
PRIO_NORMAL 
  
> A mensagem tem prioridade normal.
    
PRIO_URGENT 
  
> A mensagem é urgente.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.
    
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

