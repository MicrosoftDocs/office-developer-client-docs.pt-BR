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
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409129"
---
# <a name="prop_id"></a>PROP_ID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o identificador de propriedade de uma marca de propriedade especificada.
  
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

Cada marca de propriedade contém o tipo de propriedade na palavra de ordem baixa (bits 0 a 15) e o identificador da propriedade na palavra de ordem alta (bits 16 a 31). A **PROP_ID** macro extrai o identificador de propriedade e o coloca nos bits 0 a 15 do inteiro a ser retornado. Os bits restantes do valor de retorno são definidos como zeros. 
  
A **PROP_ID** macro pode ser usada, por exemplo, para recuperar um identificador a ser passado para [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). **GetNamesFromIDs** recupera o nome da propriedade associada a um identificador de uma propriedade nomeada. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Macros relacionadas a estruturas](macros-related-to-structures.md)

