---
title: Propriedade canônica PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fa29a55a5fc2ce89e125909d13a2c14a347ef831
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594019"
---
# <a name="pidlidsideeffects-canonical-property"></a>Propriedade canônica PidLidSideEffects

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Controla como um objeto de mensagem é manipulado pelo cliente quando atuando na entrada do usuário final.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSideEffects  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x00008510  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuração de tempo de execução  <br/> |
   
## <a name="remarks"></a>Comentários

Deve ser definido como um bit a bit ou zero ou mais dos seguintes sinalizadores.
  
|**Name**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Processamento adicional é necessária no objeto mensagem ao excluir.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Nenhuma interface de usuário está associado com o objeto de mensagem.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Processamento adicional é necessária no objeto mensagem ao mover ou copiar a um objeto de pasta com uma propriedade **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de "Falha de página inválida. Observe".  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |Processamento adicional é necessária no objeto mensagem ao copiar para outra pasta.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Processamento adicional é necessária no objeto mensagem durante a mudança para outra pasta.  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |Processamento adicional é necessária no objeto mensagem ao exibir os verbos para o usuário final.  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |Não é possível desfazer a operação de exclusão, não deve ser definida, a menos que "seOpenToDelete" estiver definida.  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Não é possível desfazer a operação de cópia, não deve ser definida, a menos que "seOpenTocopy" estiver definida.  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |Não é possível desfazer a operação de movimentação, não deve ser definida, a menos que "seOpenToMove" estiver definida.  <br/> |
|seHasScript  <br/> |0x2000  <br/> |O objeto de mensagem contém um script do usuário final.  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |Processamento adicional é necessária para excluir permanentemente o objeto de mensagem.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

