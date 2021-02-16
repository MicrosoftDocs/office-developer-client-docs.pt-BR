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
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331294"
---
# <a name="pidlidsideeffects-canonical-property"></a>Propriedade canônica PidLidSideEffects

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Controla como um objeto de mensagem é manipulado pelo cliente ao atuar na entrada do usuário final.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSideEffects  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008510  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuração em tempo de execução  <br/> |
   
## <a name="remarks"></a>Comentários

Deve ser definido como um bit a bit ou zero ou mais dos sinalizadores a seguir.
  
|**Nome**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Processamento adicional é necessário no objeto de mensagem ao excluir.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Nenhuma interface do usuário está associada ao objeto de mensagem.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Processamento adicional é necessário no objeto de mensagem ao mover ou copiar para um objeto de pasta com uma propriedade **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de "IPF. Observação".  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |Processamento adicional é necessário no objeto de mensagem ao copiar para outra pasta.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Processamento adicional é necessário no objeto de mensagem ao mover para outra pasta.  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |Processamento adicional é necessário no objeto de mensagem ao exibir verbos para o usuário final.  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |Não é possível desfazer a operação de exclusão, não deve ser definida, a menos que "seOpenToDelete" esteja definido.  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Não é possível desfazer a operação de cópia, não deve ser definida, a menos que "seOpenTocopy" esteja definido.  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |Não é possível desfazer a operação de movimentação, não deve ser definida, a menos que "seOpenToMove" esteja definido.  <br/> |
|seHasScript  <br/> |0x2000  <br/> |O objeto message contém script do usuário final.  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |O processamento adicional é necessário para excluir permanentemente o objeto de mensagem.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definição de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

