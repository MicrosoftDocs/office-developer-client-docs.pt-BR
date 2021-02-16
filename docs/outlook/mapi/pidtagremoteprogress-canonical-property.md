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
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439839"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Propriedade canônica PidTagRemoteProgress

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa propriedade contém um número que indica o status de uma transferência remota.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Identificador:  <br/> |0x3E0B  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI Status  <br/> |
   
## <a name="remarks"></a>Comentários

Se nenhuma transferência estiver em andamento, essa propriedade deverá ser definida como 1. Se uma transferência estiver em andamento, ela deverá ser definida para um valor de 0 a 100, indicando a porcentagem de conclusão da transferência.
  
O texto associado ao código de status numérico aparece na propriedade **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).
  
Os sinalizadores a seguir podem ser definidos para essa propriedade:
  
MSGSTATUS_REMOTE_DELETE
  
> A transferência de mensagens é excluída.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> A transferência de mensagens está em andamento.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

