---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Última modificação: 23 de julho de 2011'
localization_priority: Priority
ms.openlocfilehash: 2b04ebe6d05cd72a59fe6d44c9138468fd7ddec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269990"
---
# <a name="tchar"></a>TCHAR

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma cadeia de caracteres do Win32 que pode ser usada para descrever cadeias de caracteres ANSI, DBCS ou Unicode. Para plataformas ANSI e DBCS, o TCHAR é definido da seguinte forma:
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Comentários

Para plataformas Unicode, o TCHAR é definido como sinônimo do tipo WCHAR. 
  
Os clientes MAPI podem usar o tipo de dados TCHAR para representar uma cadeia de caracteres do tipo WCHAR ou char. Certifique-se de definir o UNICODE da constante simbólica e limite a plataforma quando for necessário. O MAPI interpretará as informações da plataforma e traduzirá internamente o TCHAR para a cadeia de caracteres apropriada. O tipo de propriedade MAPI, PT_TSTRING, funciona exatamente como o tipo de dados TCHAR. Quando a plataforma suporta Unicode, as propriedades do tipo PT_TSTRING são atribuídas ao tipo PT_UNICODE no tempo de compilação. Quando a plataforma não oferece suporte a Unicode, essas propriedades são atribuídas ao tipo PT_STRING8.
  
Confira mais informações sobre essa em [Conjuntos de Caracteres](mapi-character-sets.md) e [Lista de Tipos de Propriedades](property-types.md). 
  
## <a name="see-also"></a>Confira também



[Tipos de dados MAPI](mapi-data-types.md)

