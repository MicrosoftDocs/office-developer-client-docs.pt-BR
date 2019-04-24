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
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349039"
---
# <a name="shdwpattern-cell-fill-format-section"></a>Célula ShdwPattern (Seção Fill Format)

Determina o padrão de preenchimento da sombra de uma forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Nenhum (preenchimento transparente)  <br/> |
|1  <br/> |Cor do primeiro plano sólida  <br/> |
|2 - 40  <br/> |Padrões variados  <br/> |
   
## <a name="remarks"></a>Comentários

Para definir o padrão de preenchimento, insira um número de 0 a 40, que serve como um índice para uma coleção de padrões. É possível visualizar a coleção de padrões de preenchimento na caixa de diálogo **Preenchimento** (na guia **Página Inicial**, do grupo **Forma**, clique em **Preenchimento** e em **Opções de Preenchimento**).
  
Para obter uma referência para a célula ShdwPattern pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShdwPattern  <br/> |
   
Para obter uma referência para a célula ShdwPattern pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillShdwPattern** <br/> |
   

