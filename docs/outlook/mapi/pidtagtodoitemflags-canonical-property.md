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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284480"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>Propriedade canônica PidTagToDoItemFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa uma condição sinalizada de um item de tarefas pendentes.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Identificador:  <br/> |0x0E2B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI não-transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é um campo de bit no qual cada bit deve ser definido como 1 se a condição associada na tabela a seguir se aplicar, caso contrário, 0.
  
||||
|:-----|:-----|:-----|
|Valor numérico  <br/> |Nome  <br/> |Descrição  <br/> |
|Não está presente  <br/> |N/D  <br/> |Não sinalizado  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |O objeto está sinalizando o tempo  <br/> |
|8  <br/> |todoRecipientFlagged  <br/> |Só deve ser definido em um objeto de mensagem de rascunho e significa que o objeto está sinalizado para destinatários.  <br/> |
   
Todos os bits não especificados na tabela são reservados. Eles devem ser ignorados, mas devem ser preservados se estiverem definidos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas à sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

