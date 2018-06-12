---
title: Célula PageLockReplace (seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica se o botão Substituir forma deve ser desabilitado para esta página.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772456"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Célula PageLockReplace (seção Page Properties)

Indica se o botão **Substituir forma** deve ser desabilitado para esta página. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O botão **Alterar forma** estiver esmaecido quando esta página estiver ativa.  <br/> |
|FALSO  <br/> |O botão **Alterar forma** não está desabilitado por esta página. O botão pode ainda ser acinzentado if: o **DocLockReplace** em **DocumentSheet** estiver definida como **TRUE**; a célula **LockReplace** para a forma selecionada é definida como **TRUE**.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Para fazer referência à célula **PageLockReplace** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageLockReplace  <br/> |
   
Para obter uma referência à célula **PageLockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageLockReplace** <br/> |
   

