---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ad4b9d3f7c2ca1766ecca4fe9467fc49098f2212
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770187"
---
# <a name="propid"></a>PROP_ID

  
  
**Aplica-se a**: Outlook 
  
Retorna o identificador de propriedade de uma marca de propriedade especificado.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Parâmetros

 _ulPropTag_
  
> Marca de propriedade que contém o identificador a ser retornado.
    
## <a name="remarks"></a>Comentários

A marca de cada propriedade contém o tipo de propriedade da palavra de ordem baixa (0 a 15 bits) e o identificador de propriedade da palavra de ordem alta (16 a 31 bits). A macro **PROP_ID** extrai o identificador de propriedade e a coloca em bits 0 a 15 do inteiro a ser retornado. Os bits restantes do valor de retorno são definidos com zeros. 
  
A macro **PROP_ID** pode ser usada, por exemplo, para recuperar um identificador a serem passados para [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). **GetNamesFromIDs** recupera o nome da propriedade associado a um identificador para uma propriedade nomeada. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

