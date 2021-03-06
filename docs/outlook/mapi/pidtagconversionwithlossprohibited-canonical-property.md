---
title: Propriedade canônica PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417123"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Propriedade canônica PidTagConversionWithLossProhibited

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se um agente de transferência de mensagens (MTA) é proibido de fazer conversões de texto de mensagem que perdem informações. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Identificador:  <br/> |0x000D  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuração geral  <br/> |
   
## <a name="remarks"></a>Comentários

Um exemplo do tipo de conversão que está sendo proibido é o mapeamento "lossy" de Unicode (dois bytes por caractere) para um conjunto de caracteres de um único byte. 
  
## <a name="related-resources"></a>Recursos relacionados

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

