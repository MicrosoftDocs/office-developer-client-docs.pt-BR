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
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435037"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a>Célula ShdwForegndTrans (Seção Fill Format)

Determina o nível de transparência para a cor utilizada para o primeiro plano (traço) do padrão de preenchimento da sombra projetada da forma.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0 - 100  <br/> |Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma sombra com preenchimento completamente transparente tenha a mesma forma que uma sombra sem preenchimento na página de desenho, ela interage com outros objetos na página da mesma forma que se a transparência fosse 0%.
  
Você pode também definir o valor utilizando o controle deslizante na caixa de diálogo **Sombra** (na guia **Página Inicial**, no grupo **Forma**, clique em **Sombra** e em **Opções de Sombra**). Esse valor controla o valor das transparências de sombra do primeiro plano e do plano de fundo. Para definir os valores independentemente, insira-os na janela ShapeSheet.
  
Para obter uma referência para a célula ShdwForegndTrans pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ShdwForegndTrans  <br/> |
   
Para obter uma referência para a célula ShdwForegndTrans pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowFill** <br/> |
|Índice de célula:  <br/> |**visFillShdwForegndTrans** <br/> |
   

