---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a187245b2594282bc9908b3075852440f418af2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766498"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Aplica-se a**: Outlook 
  
Descreve a caixa de diálogo que é construída a partir de uma tabela de exibição pela função [BuildDisplayTable](builddisplaytable.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a>Members

 **cctl**
  
> Contagem de controles apontado pelo membro **lpctl** . 
    
 **lpszResourceName**
  
> Ponteiro para o nome ou número inteiro identificador para o recurso de caixa de diálogo. 
    
 **lpszComponent**
  
> Ponteiro para a cadeia de caracteres que aparece na seção **[Help File Mappings]** em MAPISVC. Como **lpszComponent** está em uma união com o membro **ulItemID** , somente um desses membros tem dados válidos. 
    
 **ulItemID**
  
> Identificador de recurso inteiro com um valor menor ou igual a 65535 do qual o nome do arquivo de Ajuda pode ser lidas. Como **ulItemID** está em uma união com o membro **lpszComponent** , somente um desses membros tem dados válidos. 
    
 **lpctl**
  
> Ponteiro para uma matriz de estruturas [DTCTL](dtctl.md) , um para cada controle na página. 
    
## <a name="remarks"></a>Comentários

Para identificar o arquivo de ajuda para a página com guias, defina o membro **lpszComponent** para uma cadeia de caracteres codificada ou o membro **ulItemID** como um identificador de recurso inteiro. 
  
Cada entrada na seção **[Help File Mappings]** em MAPISVC. INF consiste em uma cadeia de componente, não mais de 30 caracteres, no lado esquerdo e um caminho de arquivo de ajuda à direita. **UlItemID** e o **lpszResourceName** são encontrados no parâmetro _hInstance_ do **BuildDisplayTable**. Para obter mais informações, consulte [MAPISVC. Seção do INF [mapeamentos do arquivo de ajuda]](mapisvc-inf-help-file-mappings-section.md).
  
Embora **BuildDisplayTable** usa essa estrutura para criar a tabela de exibição de recursos de controle, a estrutura **DTPAGE** nunca será exibida na tabela a exibição em si. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

