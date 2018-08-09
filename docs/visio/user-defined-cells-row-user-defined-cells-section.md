---
title: Linha User-defined Cells (Seção User-defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Contém o valor e o prompt descritivo para qualquer célula definida pelo usuário na solução. Uma forma contém uma linha User-defined Cells para cada par de célula Value/Prompt definida pelo usuário.
ms.openlocfilehash: 45a9a033fe486a14e9881c3d79b79a129ecedc1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773223"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>Linha User-defined Cells (Seção User-defined Cells)

Contém o valor e o prompt descritivo para qualquer célula definida pelo usuário na solução. Uma forma contém uma linha User-defined Cells para cada par de célula Value/Prompt definida pelo usuário.
  
Linhas de células definidas pelo usuário são denominadas User. *nome* e contém as células a seguir. Para obter mais detalhes, consulte os tópicos de célula específica. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[Valor](value-cell-user-defined-cells-section.md) <br/> |Especifica um valor para a célula definida pelo usuário correspondente.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Especifica um comentário ou prompt descritivo para a célula definida pelo usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

Células definidas pelo usuário podem ser usadas para inserir fórmulas ou constantes que são referenciadas por outras células ou outros complementos. Os valores nas células definidas pelo usuário são portáteis, isto é, se uma forma que faz referência a uma célula definida pelo usuário em uma forma for copiada para outra forma que não tenha a mesma célula definida pelo usuário, a célula será adicionada à forma.
  
 Você pode adicionar tantos usuários.  linhas de *nome* conforme necessário, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar uma linha a uma seção User-defined Cells existente, do mouse em uma linha e clique em **Inserir linha** no menu de atalho. 
  
Você pode fazer referência a essas células pelo nome da linha, exibido em uma janela ShapeSheet em texto vermelho. Para atribuir nomes significativos ao usuário. linhas de *nome* , clique na linha e digite um nome como *Deslocar* , por exemplo, para criar o nome da linha offset. Você pode fazer referência à célula Prompt usando User.Offset.Prompt. 
  
O nome de linha inserido deve ser único na seção.
  

