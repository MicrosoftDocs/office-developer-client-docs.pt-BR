---
title: Célula PageLockDuplicate (seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina se a página pode ser duplicada, como um Boolean.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425978"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>Célula PageLockDuplicate (seção Page Properties)

Determina se a página pode ser duplicada, como um Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplicata** no menu de atalho da página e o método de automação **Page. Duplicate** estão desabilitados para a página.  <br/> |
|FALSE  <br/> |A página pode ser duplicada.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **PageLockDuplicate** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | PageLockDuplicate  <br/> |
   
Para obter uma referência para a célula **PageLockDuplicate** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowPage** <br/> |
| Índice de célula:  <br/> |**visPageLockDuplicate** <br/> |
   

