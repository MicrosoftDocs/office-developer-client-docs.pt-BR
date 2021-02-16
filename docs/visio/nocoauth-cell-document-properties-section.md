---
title: Célula NoCoauth (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou no Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautor.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420511"
---
# <a name="nocoauth-cell-document-properties-section"></a>Célula NoCoauth (Seção Document Properties)

Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou no Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautor.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O documento não pode ser coautor e está bloqueado para edição quando aberto.  <br/> |
|FALSE  <br/> |O documento pode ser coautor.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **NoCoauth** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | NoCoauth  <br/> |
   
Para fazer referência à célula **NoCoauth** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowDoc** <br/> |
| Índice de célula:  <br/> |**visDocNoCoauth** <br/> |
   

