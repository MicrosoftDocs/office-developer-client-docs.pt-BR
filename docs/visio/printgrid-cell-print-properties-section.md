---
title: Célula PrintGrid (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033794
localization_priority: Normal
ms.assetid: 0504ff7f-2274-7ae3-1f4b-a3d890dbd79a
description: Especifica se a grade será impressa ao imprimir a página de um documento.
ms.openlocfilehash: 9b98999cd02fa6a47ec8564bbd7337ecf8637306
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433203"
---
# <a name="printgrid-cell-print-properties-section"></a>Célula PrintGrid (Seção Print Properties)

Especifica se a grade será impressa ao imprimir a página de um documento.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Mostra a grade ao imprimir a página.  <br/> |
|FALSE  <br/> |Não mostra a grade ao imprimir a página (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Esse valor corresponde à caixa de seleção **Linhas de grade** da guia **Configurar Impressão** da caixa de diálogo **Configurar Página** (na guia **Design**, clique na seta **Configurar Página**). Fora a cor (a versão impressa é cinza), a grade impressa é idêntica à grade que você vê na janela de desenho do Microsoft Visio. 
  
Você pode imprimir a grade página por página. O estilo da grade também pode ser definido em uma base página por página na caixa de diálogo **grade &amp; da régua** (na guia **Exibir** , clique na seta **Mostrar** ) quando uma página estiver ativa. 
  
Para obter uma referência para a célula PrintGrid pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PrintGrid  <br/> |
   
Para obter uma referência para a célula PrintGrid pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPrintProperties** <br/> |
|Índice da célula:  <br/> |**visPrintPropertiesPrintGrid** <br/> |
   

