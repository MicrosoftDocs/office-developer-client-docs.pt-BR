---
title: Célula Label (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Especifica o rótulo exibido aos usuários na janela Dados da Forma. Um rótulo consiste em caracteres alfanuméricos, incluindo o caractere de sublinhado (_).
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420175"
---
# <a name="label-cell-shape-data-section"></a>Célula Label (Seção Shape Data)

Especifica o rótulo exibido aos usuários na janela **Dados da Forma**. Um rótulo consiste em caracteres alfanuméricos, incluindo o caractere de sublinhado (_). 
  
## <a name="remarks"></a>Comentários

O aplicativo inclui automaticamente a cadeia de caracteres do rótulo entre aspas na célula, embora as aspas não sejam exibidas na janela **Dados da Forma**. 
  
Se nenhum texto para o rótulo for localizado, o Visio exibirá o nome da linha (Prop.Linha) na janela **Dados da Forma**. 
  
Para obter uma referência para a célula Label pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Hélice. *Nome* . Rótulo em que prop.  *Name* é o nome da linha  <br/> |
   
Para obter uma referência para a célula Label pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionProp** <br/> |
|Índice de linha:  <br/> |**visRowProp** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCustPropsLabel** <br/> |
   

