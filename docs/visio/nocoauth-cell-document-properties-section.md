---
title: Célula NoCoauth (seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautoria.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319436"
---
# <a name="nocoauth-cell-document-properties-section"></a>Célula NoCoauth (seção Document Properties)

Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautoria.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |O documento não pode ser coautoria e está bloqueado para edição quando aberto.  <br/> |
|FALSE  <br/> |O documento pode ser coautoria.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma referência para a célula **NoCoauth** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | NoCoauth  <br/> |
   
Para obter uma referência para a célula **NoCoauth** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |**visDocNoCoauth** <br/> |
   

