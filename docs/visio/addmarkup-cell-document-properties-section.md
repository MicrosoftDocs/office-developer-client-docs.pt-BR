---
title: Célula AddMarkup (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Indica se as marcações do documento estão sendo revisadas.
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427630"
---
# <a name="addmarkup-cell-document-properties-section"></a>Célula AddMarkup (Seção Document Properties)

Indica se as marcações do documento estão sendo revisadas.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O documento está sendo revisado.  <br/> |
|FALSE  <br/> |O documento não está sendo revisado (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Quando a célula AddMarkup está definida como VERDADEIRO, o revisor está adicionando marcações e as alterações são aplicadas às páginas de sobreposição de marcação, e não às páginas de desenho originais. Quando a célula AddMarkup está definida como FALSO, o controle de marcação está desativado e as alterações são aplicadas às páginas de desenho originais.
  
> [!NOTE]
> Você pode impedir a marcação em seus documentos usando a função GUARD. Se a célula addMarkup contiver a fórmula = GUARD (FALSE), o comando **rastrear marcação** será desabilitado. 
  
Essa configuração corresponde à configuração de comando **Rastrear Marcação** no grupo **Marcação** na guia **Revisão**. 
  
Para fazer referência à célula AddMarkup pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |AddMarkup  <br/> |
   
Para fazer referência à célula AddMarkup pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowDoc** <br/> |
|Índice da célula:  <br/> |**visDocAddMarkup** <br/> |
   

