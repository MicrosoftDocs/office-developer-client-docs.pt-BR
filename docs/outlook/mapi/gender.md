---
title: Gênero
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766646"
---
# <a name="gender"></a>Gênero

  
  
**Aplica-se a**: Outlook 
  
Especifica os valores possíveis para o gênero de um usuário de mensagens.
  
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
  
> O número mínimo de diferentes valores suportados para o gênero.
    
 _genderUnspecified_
  
> O gênero não for especificado para o usuário de mensagens.
    
 _genderFemale_
  
> O usuário de mensagens é feminino.
    
 _genderMale_
  
> O usuário de mensagens é Masculino.
    
 _genderCount_
  
> O número de diferentes valores suportados para o gênero.
    
 _genderMax_
  
> O número máximo de diferentes valores suportados para o gênero.
    
## <a name="see-also"></a>Confira também



[Propriedade canônico de PidTagGender](pidtaggender-canonical-property.md)

