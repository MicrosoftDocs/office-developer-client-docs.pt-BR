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
ms.openlocfilehash: d8d986554352e05398a843723ee802bb4969e5ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769819"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>Propriedade canônica PidTagRemoteValidateOk

  
  
**Aplica-se a**: Outlook 
  
Essa propriedade contém TRUE se o visualizador remoto tiver permissão para chamar o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|Identificador:  <br/> |0x3E0D  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é exibido na tabela de status e oferece algum controle sobre o desempenho de transporte. Ele pode ser considerado como outra forma de direcionar o visualizador remoto em ocioso. Quando ele for definido como TRUE, o visualizador remoto pode chamar **IMAPIStatus::ValidateState** quantas vezes quiser. Um valor FALSE indica que o visualizador remoto não é possível fazer todas as chamadas mais. 
  
O provedor de transporte normalmente faz essa propriedade dinamicamente, definindo o valor como FALSE para desativar chamadas adicionais quando o provedor de transporte tem uma quantidade suficiente de processamento para executar. Quando é feito o provedor de transporte, ele define o valor como TRUE para permitir que o aplicativo cliente para fazer chamadas de **IMAPIStatus::ValidateState** de adicionais. 
  
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

