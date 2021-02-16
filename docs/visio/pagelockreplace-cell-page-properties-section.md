---
title: Célula PageLockReplace (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica se o botão Substituir Forma deve ser desabilitado para esta página.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433098"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Célula PageLockReplace (Seção Page Properties)

Indica se o botão **Substituir Forma** deve ser desabilitado para esta página. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O **botão Alterar** Forma fica es cinza quando esta página está ativa.  <br/> |
|FALSE  <br/> |O **botão Alterar** Forma não está desabilitado por esta página. O botão ainda poderá ficar es cinza se: **o DocLockReplace** na **Planilha de Documentos** estiver definido como **VERDADEIRO**; a **célula LockReplace** para a forma selecionada é definida como **TRUE**.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **PageLockReplace** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageLockReplace  <br/> |
   
Para fazer referência à célula **PageLockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPage** <br/> |
| Índice de célula:  <br/> |**visPageLockReplace** <br/> |
   

