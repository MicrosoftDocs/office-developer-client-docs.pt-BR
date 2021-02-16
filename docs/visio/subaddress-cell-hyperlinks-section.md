---
title: Célula SubAddress (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Especifica uma localidade no documento de destino à qual vincular.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349319"
---
# <a name="subaddress-cell-hyperlinks-section"></a>Célula SubAddress (Seção Hyperlinks)

Especifica uma localidade no documento de destino à qual vincular.
  
## <a name="remarks"></a>Comentários

Por exemplo, se a célula Address for "Drawing1.vsdx", a célula SubAddress poderá especificar um nome de página como "Page-3". Se a célula Address for o arquivo do Microsoft Excel "Samples.xlsx", o valor dessa célula poderá ser uma planilha ou um intervalo dentro de uma planilha, como "Funções de Planilha" ou "Planilha1! A1:D10". Se a célula Address for " ", o valor dessa célula poderá ser uma âncora nomeada dentro do https://www.microsoft.com/office/ documento, como "soluções".
  
Você pode também definir o valor da célula utilizando a caixa de diálogo **Hiperlinks** (no grupo **Links** da guia **Inserir**, clique em **Hyperlink**).
  
Para obter uma referência para a célula SubAddress pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *nome*  . SubAddress onde Hyperlink  *.name é*  o nome da linha  <br/> |
   
Para fazer referência à célula **SubAddress** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHiperlink** <br/> |
| Índice de linha:  <br/> |**visRow1stHyperlink**  +   *i* onde *i* = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visHLinkSubAddress** <br/> |
   

