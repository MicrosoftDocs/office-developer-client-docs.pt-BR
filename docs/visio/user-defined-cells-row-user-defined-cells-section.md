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
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420686"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>Linha User-defined Cells (Seção User-defined Cells)

Contém o valor e o prompt descritivo para qualquer célula definida pelo usuário na solução. Uma forma contém uma linha User-defined Cells para cada par de célula Value/Prompt definida pelo usuário.
  
As linhas User-defined Cells são denominadas User. *nome* e contém as células a seguir. Para obter mais detalhes, consulte os tópicos específicos das células. 
  
|**Célula**|**Descrição**|
|:-----|:-----|
|[Valor](value-cell-user-defined-cells-section.md) <br/> |Especifica um valor para a célula definida pelo usuário correspondente.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Especifica um comentário ou prompt descritivo para a célula definida pelo usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

Células definidas pelo usuário podem ser usadas para inserir fórmulas ou constantes que são referenciadas por outras células ou outros complementos. Os valores nas células definidas pelo usuário são portáteis, isto é, se uma forma que faz referência a uma célula definida pelo usuário em uma forma for copiada para outra forma que não tenha a mesma célula definida pelo usuário, a célula será adicionada à forma.
  
 É possível adicionar tantas linhas User.  *name* quantas forem necessárias, atribuir nomes significativos às linhas e definir valores de célula. Para adicionar uma linha a uma seção User-defined Cells existente, clique com o botão direito do mouse em uma linha e clique em **Inserir Linha** no menu de atalho. 
  
É possível fazer referência a essas células pelo nome da linha, exibido na janela ShapeSheet em texto vermelho. Para atribuir nomes significativos às linhas User. *nomear* linhas, clique na linha e digite um nome como *deslocamento* , por exemplo, para criar o nome da linha user. Offset. Você pode fazer referência à célula Prompt usando User.Offset.Prompt. 
  
O nome de linha inserido deve ser único na seção.
  

