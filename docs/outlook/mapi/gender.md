---
title: Gênero
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428645"
---
# <a name="gender"></a>Gênero

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica os valores possíveis para o sexo de um usuário de mensagens.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a>Membros

 _genderMin_
  
> O número mínimo de valores diferentes com suporte para o sexo.
    
 _genderUnspecified_
  
> O sexo não é especificado para o usuário de mensagens.
    
 _genderFemale_
  
> A usuária de mensagens é mulher.
    
 _genderMale_
  
> O usuário de mensagens é adulto.
    
 _genderCount_
  
> O número de valores diferentes com suporte para o sexo.
    
 _genderMax_
  
> O número máximo de valores diferentes com suporte para o sexo.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagGender](pidtaggender-canonical-property.md)

