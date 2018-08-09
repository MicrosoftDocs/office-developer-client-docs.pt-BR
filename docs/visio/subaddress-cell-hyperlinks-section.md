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
ms.openlocfilehash: 0509b9b6a708924b5aeb69f16f3f4cd99573cc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773087"
---
# <a name="subaddress-cell-hyperlinks-section"></a>Célula SubAddress (Seção Hyperlinks)

Especifica uma localidade no documento de destino à qual vincular.
  
## <a name="remarks"></a>Comentários

Por exemplo, se a célula Address for "Drawing1.vsdx", a célula SubAddress pode especificar um nome de página como "Página-3". Se a célula Address for o arquivo do Microsoft Excel "Samples.xlsx", o valor dessa célula pode ser uma planilha ou um intervalo em uma planilha, como "Funções de planilha" ou "Sheet1! A1: D10 ". Se a célula Address for "http://www.microsoft.com/office/", o valor dessa célula pode ser uma âncora nomeada dentro do documento, como "soluções".
  
Você pode também definir o valor da célula utilizando a caixa de diálogo **Hiperlinks** (no grupo **Links** da guia **Inserir**, clique em **Hyperlink**).
  
Para obter uma referência para a célula SubAddress pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *nome* . Subendereço onde Hyperlink *. nome* é o nome da linha  <br/> |
   
Para obter uma referência para a célula **SubAddress** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
| Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visHLinkSubAddress** <br/> |
   

