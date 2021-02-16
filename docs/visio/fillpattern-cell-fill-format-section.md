---
title: Célula FillPattern (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Determina o padrão de preenchimento da forma. Para especificar um padrão de preenchimento personalizado, utilize a função USE da célula.
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422926"
---
# <a name="fillpattern-cell-fill-format-section"></a>Célula FillPattern (Seção Fill Format)

Determina o padrão de preenchimento da forma. Para especificar um padrão de preenchimento personalizado, utilize a função USE da célula.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Nenhum (preenchimento transparente).  <br/> |
|1   <br/> |Cor do primeiro plano sólida.  <br/> |
|2 - 40  <br/> |Padrões de preenchimento variados correspondentes a entradas indexadas na caixa de diálogo **Preenchimento**.  <br/> |
   
## <a name="remarks"></a>Comentários

Você pode também definir o valor utilizando a caixa de diálogo **Preenchimento** (na guia **Página Inicial**, no grupo **Forma**, clique em **Preenchimento** e em **Opções de preenchimento**).
  
Para obter uma referência para a célula FillPattern pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |FillPattern  <br/> |
   
Para obter uma referência para a célula FillPattern pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowFill** <br/> |
|Índice de célula:  <br/> |**visFillPattern** <br/> |
   

