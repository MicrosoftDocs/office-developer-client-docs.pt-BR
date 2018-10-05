---
title: Propriedade canônica PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400276"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>Propriedade canônica PidTagToDoItemFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa a condição de um item de tarefas pendentes sinalizadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Identificador:  <br/> |0x0E2B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é um campo de bit no qual cada bit deve ser definido como 1 se se aplica a condição associada na tabela a seguir, caso contrário 0.
  
||||
|:-----|:-----|:-----|
|Valor numérico  <br/> |Nome  <br/> |Descrição  <br/> |
|Não estiver presente  <br/> |N/A  <br/> |Sem sinalizador  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |Objeto é o tempo sinalizado  <br/> |
|8  <br/> |todoRecipientFlagged  <br/> |Só deve ser definido em um objeto de mensagem de rascunho e significa que o objeto foi sinalizado para destinatários.  <br/> |
   
Todos os bits que não forem especificados na tabela são reservados. Eles devem ser ignorados, mas devem ser preservados se eles estiverem definidos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas a sinalização.
    
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

