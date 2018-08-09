---
title: Célula NoCoauth (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautoria.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772417"
---
# <a name="nocoauth-cell-document-properties-section"></a>Célula NoCoauth (Seção Document Properties)

Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautoria.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |O documento não pode ser coautor e está bloqueado para edição quando estiver aberto.  <br/> |
|FALSO  <br/> |Pode ser coautor do documento.  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula **NoCoauth** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | NoCoauth  <br/> |
   
Para obter uma referência à célula **NoCoauth** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowDoc** <br/> |
| Índice da célula:  <br/> |**visDocNoCoauth** <br/> |
   

