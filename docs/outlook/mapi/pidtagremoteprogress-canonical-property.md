---
title: Propriedade canônica PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e1f57fd95ff38ef102cd74b0035dbb6b553259c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569348"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Propriedade canônica PidTagRemoteProgress

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa propriedade contém um número que indica o status de uma transferência remota.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Identificador:  <br/> |0x3E0B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Se nenhuma transferência estiver em andamento, essa propriedade deverá ser definida como 1. Se uma transferência estiver em andamento, ela deve ser definida como um valor de 0 a 100 que indica a porcentagem da transferência de conclusão.
  
O texto associado ao código de status numérica é exibida na propriedade **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).
  
Sinalizadores a seguir podem ser definidos para essa propriedade:
  
MSGSTATUS_REMOTE_DELETE
  
> A transferência de mensagem é excluída.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> A transferência de mensagem está em andamento.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

