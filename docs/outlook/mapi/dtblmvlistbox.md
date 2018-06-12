---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766480"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Aplica-se a**: Outlook 
  
Descreve uma lista de valores múltiplos que será exibida em uma caixa de diálogo que é construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Membros

 **ulFlags**
  
> Reservado; deve ser zero.
    
 **ulMVPropTag**
  
> Marca de propriedade para uma propriedade de valores múltiplos do tipo PT_MV_TSTRING.
    
## <a name="remarks"></a>Coment�rios

Uma estrutura **DTBLMVLISTBOX** descreve uma lista de valores múltiplos padrão que tem uma lista de itens de somente leitura. Usando uma lista de valores múltiplos padrão, os valores são exibidos imediatamente. 
  
Os dados que são exibidos provêm a propriedade identificada no membro **ulMVPropTag** . Não há nenhum requisito para a interface de propriedade que está associada com a tabela de exibição de leitura. Além disso, como os usuários não são capazes de realizar seleções desses tipos de listas, dados não são gravados na interface de propriedade. 
  
Somente as propriedades de cadeia de caracteres de valores múltiplos são suportadas para a lista de valores múltiplos; Não há suporte para outros tipos de propriedade de valores múltiplos. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

