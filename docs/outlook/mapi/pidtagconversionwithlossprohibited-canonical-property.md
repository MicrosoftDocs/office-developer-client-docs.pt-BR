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
ms.openlocfilehash: eee70d97c35c7f115e424905b9e36f3dfa392c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769146"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Propriedade canônica PidTagConversionWithLossProhibited

  
  
**Aplica-se a**: Outlook 
  
Conterá TRUE se um agente de transferência de mensagem (MTA) é proibido de fazerem conversões de texto que perdem informações de mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Identificador:  <br/> |0x000D  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuração geral  <br/> |
   
## <a name="remarks"></a>Comentários

Um exemplo do tipo de conversão que está sendo proibida é o mapeamento "com perdas" do Unicode (dois bytes por caractere) para um conjunto de caracteres de byte único. 
  
## <a name="related-resources"></a>Recursos relacionados

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

