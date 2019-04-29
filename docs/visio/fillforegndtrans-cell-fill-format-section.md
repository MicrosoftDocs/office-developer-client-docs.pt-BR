---
title: Célula FillForegndTrans (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: Determina o nível de transparência para a cor do primeiro plano (preenchimento) do padrão de preenchimento da forma.
ms.openlocfilehash: d05a83f83ea3d95ac3d42a2bfb3996917119f580
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427847"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a>Célula FillForegndTrans (Seção Fill Format)

Determina o nível de transparência para a cor do primeiro plano (preenchimento) do padrão de preenchimento da forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0 - 100  <br/> |Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma forma com preenchimento completamente transparente tenha a mesma aparência de uma forma sem preenchimento na página de desenho, ela irá interagir com os outros objetos da página da mesma forma que se a transparência fosse 0%.
  
Você pode também definir o valor utilizando o controle deslizante na caixa de diálogo **Preenchimento** (na guia **Página Inicial**, no grupo **Forma**, clique em **Preenchimento** e em **Opções de preenchimento**). Esse valor controla o valor das transparências de preenchimento do primeiro plano e do plano de fundo. Para definir os valores independentemente, insira-os na janela ShapeSheet.
  
Para obter uma referência para a célula FillForegndTrans pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |FillForegndTrans  <br/> |
   
Para obter uma referência para a célula FillForegndTrans pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowFill** <br/> |
|Índice da célula:  <br/> |**visFillForegndTrans** <br/> |
   

