---
title: Célula ShdwPattern (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Determina o padrão de preenchimento da sombra de uma forma.
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772947"
---
# <a name="shdwpattern-cell-fill-format-section"></a>Célula ShdwPattern (Seção Fill Format)

Determina o padrão de preenchimento da sombra de uma forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Nenhum (preenchimento transparente)  <br/> |
|1  <br/> |Cor do primeiro plano sólida  <br/> |
|2 - 40  <br/> |Padrões variados  <br/> |
   
## <a name="remarks"></a>Comentários

Para definir o padrão de preenchimento, insira um número de 0 a 40, que é um índice em uma coleção de padrões. Você pode exibir a coleção de padrões de preenchimento na caixa de diálogo **preenchimento** (na guia **página inicial** , no grupo **forma** , clique em **preenchimento**e, em seguida, clique em **Opções de preenchimento**).
  
Para obter uma referência para a célula ShdwPattern pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShdwPattern  <br/> |
   
Para obter uma referência para a célula ShdwPattern pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillShdwPattern** <br/> |
   

