---
title: Propriedade canônica PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355612"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Propriedade canônica PidTagRemoteValidateOk

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Esta propriedade conterá TRUE se o visualizador remoto tiver permissão para chamar o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) . 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Identificador:  <br/> |0x3E0D  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade aparece na tabela status e oferece algum controle sobre o desempenho de transporte. Pode ser considerado outra maneira de direcionar o visualizador remoto para ocioso. Quando ele é definido como TRUE, o visualizador remoto pode chamar **IMAPIStatus:: ValidateState** , conforme desejado. Um valor FALSE indica que o visualizador remoto não pode fazer mais chamadas. 
  
O provedor de transporte geralmente define essa propriedade dinamicamente, definindo o valor como FALSE para desabilitar chamadas adicionais quando o provedor de transporte tem uma quantidade suficiente de processamento para executar. Quando o provedor de transporte é concluído, ele define o valor como TRUE para permitir que o aplicativo cliente faça mais **IMAPIStatus:: ValidateState** calls. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

