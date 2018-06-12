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
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771268"
---
# <a name="addmarkup-cell-document-properties-section"></a>Célula AddMarkup (Seção Document Properties)

Indica se as marcações do documento estão sendo revisadas.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O documento está sendo revisado.  <br/> |
|FALSO  <br/> |O documento não está sendo revisado (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Quando a célula AddMarkup está definida como TRUE, o revisor está adicionando marcações e as alterações são aplicadas às páginas de sobreposição de marcação, não às páginas de desenho originais. Quando a célula AddMarkup é FALSE, o rastreamento de marcação está desativado e as alterações são aplicadas a páginas do desenho originais.
  
> [!NOTE]
> Você pode impedir a marcação em seus documentos usando a função GUARD. Se a célula AddMarkup contém a fórmula = Guard (FALSO), o comando **Rastrear Marcação** está desabilitado. 
  
Essa configuração corresponde à configuração de comando **Rastrear Marcação** no grupo **marcação** na guia **revisão** . 
  
Para obter uma referência à célula AddMarkup pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |AddMarkup  <br/> |
   
Para obter uma referência à célula AddMarkup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowDoc** <br/> |
|Índice da célula:  <br/> |**visDocAddMarkup** <br/> |
   

