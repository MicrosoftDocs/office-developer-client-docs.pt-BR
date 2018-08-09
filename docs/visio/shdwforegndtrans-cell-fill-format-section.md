---
title: Célula ShdwForegndTrans (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Determina o nível de transparência para a cor utilizada para o primeiro plano (traço) do padrão de preenchimento da sombra projetada da forma.
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772940"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>Célula ShdwForegndTrans (Seção Fill Format)

Determina o nível de transparência para a cor utilizada para o primeiro plano (traço) do padrão de preenchimento da sombra projetada da forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|
          0 - 100
  <br/> |Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).  <br/> |
   
## <a name="remarks"></a>Comentários

Valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma sombra com preenchimento completamente transparente aparece na página de desenho da mesma como uma sombra que não tenha preenchimento, ele se interage com outros objetos na página da mesma forma como se a transparência fosse 0%.
  
Você pode também definir o valor utilizando o controle deslizante na caixa de diálogo **Sombra** (na guia **Página Inicial**, no grupo **Forma**, clique em **Sombra** e em **Opções de Sombra**). Esse valor controla o valor das transparências de sombra do primeiro plano e do plano de fundo. Para definir os valores independentemente, insira-os na janela ShapeSheet.
  
Para obter uma referência para a célula ShdwForegndTrans pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShdwForegndTrans  <br/> |
   
Para obter uma referência para a célula ShdwForegndTrans pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillShdwForegndTrans** <br/> |
   

