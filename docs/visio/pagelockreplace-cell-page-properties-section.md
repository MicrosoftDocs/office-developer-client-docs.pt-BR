---
title: Célula PageLockReplace (seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica se o botão substituir forma deve ser desativado para esta página.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339477"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Célula PageLockReplace (seção Page Properties)

Indica se o botão **substituir forma** deve ser desativado para esta página. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |O botão **alterar forma** fica esmaecido quando esta página está ativa.  <br/> |
|FALSE  <br/> |O botão **alterar forma** não está desabilitado por esta página. O botão ainda pode estar esmaecido se: o **DocLockReplace** no **DocumentSheet** é definido como **true**; a célula **LockReplace** da forma selecionada é definida como **true**.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **PageLockReplace** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageLockReplace  <br/> |
   
Para obter uma referência para a célula **PageLockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageLockReplace** <br/> |
   

