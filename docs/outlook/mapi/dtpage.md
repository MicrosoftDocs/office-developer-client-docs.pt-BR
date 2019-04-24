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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287101"
---
# <a name="dtpage"></a>DTPAGE

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve a caixa de diálogo criada a partir de uma tabela de exibição pela função [BuildDisplayTable](builddisplaytable.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Contagem de controles apontados pelo membro **lpctl** . 
    
 **lpszResourceName**
  
> Ponteiro para o nome ou identificador de inteiro do recurso da caixa de diálogo. 
    
 **lpszComponent**
  
> Ponteiro para a cadeia de caracteres exibida na seção **[help file Mappings]** no MAPISVC. inf. Como **lpszComponent** está em uma União com o membro **ulItemID** , somente um desses membros tem dados válidos. 
    
 **ulItemID**
  
> Identificador de recurso inteiro com um valor menor ou igual a 65535 do qual o nome do arquivo de ajuda pode ser lido. Como **ulItemID** está em uma União com o membro **lpszComponent** , somente um desses membros tem dados válidos. 
    
 **lpctl**
  
> Ponteiro para uma matriz de estruturas [DTCTL](dtctl.md) , uma para cada controle na página. 
    
## <a name="remarks"></a>Comentários

Para identificar o arquivo de ajuda para a página com guias, defina o membro **lpszComponent** como uma cadeia de caracteres embutida em código ou o membro **ulItemID** como um identificador de recurso inteiro. 
  
Cada entrada na seção **[arquivos de ajuda mapeamentos]** no MAPISVC. INF consiste em uma cadeia de caracteres de componente, não mais de 30 caracteres, no lado esquerdo e um caminho de arquivo de ajuda à direita. Tanto **ulItemID** quanto **lpszResourceName** são encontrados no parâmetro _HINSTANCE_ de **BuildDisplayTable**. Para obter mais informações, consulte [MAPISVC. INF [mapeamentos de arquivos de ajuda] seção](mapisvc-inf-help-file-mappings-section.md).
  
Embora o **BuildDisplayTable** Use essa estrutura para criar a tabela de exibição a partir de recursos de controle, a estrutura do **DTPAGE** nunca aparece na própria tabela de exibição. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)
  
[DTBLPAGE](dtblpage.md)
  
[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

