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
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588451"
---
# <a name="gender"></a>Gênero

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

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

