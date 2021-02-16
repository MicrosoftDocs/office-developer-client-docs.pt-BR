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
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408219"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve a caixa de diálogo criada a partir de uma tabela de exibição pela [função BuildDisplayTable.](builddisplaytable.md) 
  
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
  
> Contagem de controles apontados pelo **membro lpctl.** 
    
 **lpszResourceName**
  
> Ponteiro para o nome ou identificador inteiro do recurso da caixa de diálogo. 
    
 **lpszComponent**
  
> Ponteiro para a cadeia de caracteres que aparece na seção **[Mapeamentos** de Arquivo de Ajuda] em MAPISVC.INF. Como **lpszComponent** está em uma união com o membro **ulItemID,** apenas um desses membros tem dados válidos. 
    
 **ulItemID**
  
> Identificador de recurso integer com um valor menor ou igual a 65535 a partir do qual o nome do arquivo de Ajuda pode ser lido. Como **ulItemID** está em uma união com o membro **lpszComponent,** apenas um desses membros tem dados válidos. 
    
 **lpctl**
  
> Ponteiro para uma matriz de [estruturas DTCTL,](dtctl.md) um para cada controle na página. 
    
## <a name="remarks"></a>Comentários

Para identificar o arquivo de Ajuda para a página com guias, de definir o membro **lpszComponent** como uma cadeia de caracteres embutida em código ou o membro **ulItemID** como um identificador de recurso inteiro. 
  
Cada entrada na seção **[Mapeamentos de Arquivo de Ajuda]** no MAPISVC. INF consiste em uma cadeia de caracteres de componente, não mais do que 30 caracteres, no lado esquerdo e um caminho de arquivo de Ajuda à direita. Tanto **ulItemID** quanto **lpszResourceName são** encontrados no  _parâmetro hInstance_ de **BuildDisplayTable**. Para obter mais informações, consulte [MAPISVC. Seção INF [Mapeamentos de Arquivos de Ajuda]](mapisvc-inf-help-file-mappings-section.md).
  
Embora **BuildDisplayTable** use essa estrutura para criar a tabela de exibição a partir de recursos de controle, a estrutura **DTPAGE** nunca aparece na própria tabela de exibição. 
  
Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md) Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

